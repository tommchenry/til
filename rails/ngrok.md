# Ngrok

It's not Rails-specific, but Rails is how I've used it. Ngrok lets you open a port on your local computer for a secure connection of a type you define. In practice that means you can say

```
ngrok http 3000
```

and open your rails server to outside traffic at the gnarly-looking termporary ngrok URL. Users hitting that URL then get routed by ngrok to the port you specified.
