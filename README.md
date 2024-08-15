# Running

```bash
npm i
npx netlify dev
```

# Querying

```bash
curl http://localhost:9999/.netlify/functions/test_fn
```

# Expected result

Just the word `hello` should be printed.

# Actual result

The output from `npx netlify dev`:
```
◈ Function test_fn has returned an error: connect ECONNREFUSED 127.0.0.1:43279
Error: connect ECONNREFUSED 127.0.0.1:43279
    at TCPConnectWrap.afterConnect [as oncomplete] (node:net:1494:16)
```

The output from `curl`:
```Error: connect ECONNREFUSED 127.0.0.1:43279
 Error: connect ECONNREFUSED 127.0.0.1:43279
    at TCPConnectWrap.afterConnect [as oncomplete] (node:net:1494:16)
```

Note that the port numbers in the error messages are always random.

