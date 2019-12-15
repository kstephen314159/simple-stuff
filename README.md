It is easy to get this to build _and_ deploy, but I'm trying to keep this simple. So at this point, one can do a maven build
first, to produce the war file in the "target" dir. And then check it in, and then use new-app to point to this git repo

```
oc new-app --name=simple https://github.com/kstephen314159/simple-stuff.git
oc expose svc simple
```

And then, `curl -v http://<hostname for route>/simple-stuff/simple/simon`
