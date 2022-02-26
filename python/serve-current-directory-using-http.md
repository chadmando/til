# Serve Current Directory Using HTTP

From the terminal, start serving the current directory using http:

```bash
python3 -m http.server
```

The default port is 8000.
To view in a browser, navigate to `http://localhost:8000`.

If you want to use a different port, add the port number to the end of the command.

```bash
python3 -m http.server 9000
```

To stop the server, use `Ctrl + C` in the terminal where the server is running.

## References

Found in many places on the web, including this [blog post](https://blog.nicolasmesa.co/posts/2018/09/serve-your-current-directory-with-python-and-http/).
