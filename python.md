### Deploying Python applications w/ virtualenv
https://nylas.com/blog/packaging-deploying-python/

### Run webserver for local directory - Change IP!
- [Stackoverflow link](http://stackoverflow.com/questions/12268835/is-it-possible-to-run-python-simplehttpserver-on-localhost-only)
- `python -c 'import BaseHTTPServer as bhs, SimpleHTTPServer as shs; bhs.HTTPServer(("127.0.0.1", 8888), shs.SimpleHTTPRequestHandler).serve_forever()'`
