---
layout: blog
title: ChatGPT, Onedrive et Blog
tags: [chatGPT, onedrive, python]
date: 2023-01-13T09:01:36.002Z
ShowWordCount: true
---
Aujourd'hui j'ai découvert [ChatGPT](https://chat.openai.com/chat), un chatbot propulsé par une IA ultra puissante à qui on peut demander de générer du code dans n'importe quel langage ! 

Je m'en suis alors servi pour écrire un code dont je rêve depuis toujours : un script de backup vers onedrive.﻿ Et oui,  tant qu'à payer un abonnement a 100 € par an pour un cloud, autant aussi y accéder aussi de manière programmatique !

C﻿hatGPT m'a donc généré le code suivant qu'il ne reste plus qu'à adapter :

```python
import shutil
import os
from onedrivesdk import Session

def backup_file_to_onedrive(file_path, client_id, client_secret):
    # Create an authenticated session
    session = Session(client_id, client_secret)

    # Get the authenticated client
    client = session.get_client()

    # Get the root folder of the OneDrive
    root_folder = client.item(drive='me', id='root').children.get()

    # Get the current date and time
    current_time = time.strftime("%Y-%m-%d %H:%M:%S", time.gmtime())

    # Get the backup file name
    backup_file_name = os.path.basename(file_path) + ' ' + current_time

    # Create a new file in the OneDrive root folder
    client.item(drive='me', id='root').children[backup_file_name].upload(file_path)

    print(f'File {file_path} has been backed up to OneDrive as {backup_file_name}.')
```

S﻿ur un autre sujet, je compte me remettre à apprendre Django, et plus généralement me dérouiller dans le domaine du web. Cela va me permettre notamment de créer une interface d'édition du blog en ligne, car actuellement il faut le cloner avec une clé SSH sur une machine pour pouvoir rédiger des article...

D﻿ans la bataille aura probablement lieu une fusion ou un transfert des données de ce blog vers une app Django. Je ferais en sorte alors de créer des backups automatisés via le script Python plus haut :)



*S﻿ide Note : J'ai appris que les webhooks tournent via l'émulateur de shell installé par git sur windows*