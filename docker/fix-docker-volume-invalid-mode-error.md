# Fix Docker Volume Invalid Mode Error

## Original Docker Volume Command

```bash
docker run -it --rm -v ${PWD}:/malware chadmando/dssuite
```

Returned this error:

```text
docker: Error response from daemon: invalid mode: /malware.
```

To fix the error, I found this [question](https://stackoverflow.com/questions/50540721/docker-toolbox-error-response-from-daemon-invalid-mode-root-docker) on Stack Overflow.
There are many opinions on how to fix the error.
I tried variations until I found the minimal change required.

## Fixed Docker Volume Command 

```bash
docker run -it --rm -v '/${PWD}:/malware' chadmando/dssuite
```

The two changes that fixed the error:

+ Add the front slash `/` before the `${PWD}`
+ Enclose the entire volume argument in single quotes `'`
