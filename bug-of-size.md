# github

## bug synchronize
```powershell
    2024-03-20 10:38:21.921 [info]
    > git push -u DHE-iad-rem-KW12.3     DHE-R507-local-KW12.3 [73005ms]
    2024-03-20 10:38:21.922 [info]
    remote: error:
    Trace:    d40f8952b3cdbdb8d3c9778288d488a0cd749d43b510dc15cacd4b9585f28586        
    remote:

    #FIXME  
    error: See https://gh.io/lfs for more information.        
    remote:
    #FIXME  
    error:
    File JDK21/jdk-21.0.2/lib/modules is 131.55 MB;
    this exceeds     GitHubs file size limit of 100.00 MB        
    remote:
    error:
    GH001: Large files detected. You may want to try Git Large File  Storage - 
    
    https://git-lfs.github.com.    

    To https://github.com/ydh-embedded/JDK.git
     ! [remote rejected] DHE-R507-local-KW12.3 -> DHE-R507-local-KW12.3     (pre-receive hook declined)

    error: 
    failed to push some refs to 'https://github.com/ydh-embedded/JDK.git'

    2024-03-20 10:38:22.195 [info]
    > git config --get commit.template [267ms]

    2024-03-20 10:38:22.196 [info]
    > git for-each-ref --format=%(refname)
    %00%  (upstream:short)
    %00%  (objectname)  
    %00%  (upstream:track)
    %00%  (upstream:remotename)
    %00%  (upstream:remoteref)
    --ignore-case
    refs/heads/DHE-R507-local-KW12.3 refs/
    remotes/DHE-R507-local-KW12.3 [264ms]

    2024-03-20 10:38:22.335 [info]
    > git status -z -uall [135ms]

```

## FIXME


Es scheint, als ob Sie aufgrund einer Verletzung der Dateigrößenbeschränkung auf ein Problem stoßen, wenn Sie Ihr Commit auf GitHub übertragen. Die Datei JDK21/jdk-21.0.2/lib/modules ist **131,55 MB** groß und überschreitet die Dateigrößenbeschränkung von GitHub von **100 MB.**

GitHub schlägt vor, Git Large File Storage (LFS) zum Verwalten großer Dateien zu verwenden. Weitere Informationen hier finden Sie: https://git-lfs.github.com.

Um dieses Problem zu beheben, können Sie entweder:

Installieren Sie Git LFS Befolgen Sie auf Ihrem System die Anweisungen zum Verwalten großer Dateien. Nach der Installation von Git LFS können Sie die große Datei auf Git LFS migrieren und versuchen, Ihr Commit erneut zu verschieben.

Entfernen Sie die große Datei aus Ihrem Repository und begehen Sie die Änderung. Auf diese Weise können Sie Ihr Commit auf GitHub übertragen. Beachten Sie jedoch, dass das Entfernen der großen Datei sie auch aus Ihrem Git-Verlauf löscht. Wenn Sie die Datei in Ihrem Repository aufbewahren müssen, sollten Sie Git LFS verwenden.

Gehen Sie folgendermaßen vor, um die große Datei zu entfernen:

**Entfernen Sie die Datei aus Ihrem lokalen Repository:**

```powershell 
        git rm --cached JDK21/jdk-21.0.2/lib/modules
```

**Die Änderung übernehmen:**

```powershell 
        git commit -m "Remove large file"
```


**Drücken Sie das Commit auf GitHub:**

```powershell 

        git push -u DHE-iad-rem-KW12.3 DHE-R507-local-KW12.3
```

**Wenn Sie die große Datei in Ihrem Repository behalten möchten, sollten Sie sie mit Git LFS verwalten.**