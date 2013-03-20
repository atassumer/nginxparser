### Nginx Configuration Parser

An nginx configuration parser that uses Pyparsing.

Parsing:

    >>> from nginxparser import load
    >>> load(open("/etc/nginx/sites-enabled/foo.conf"))

     [['server'], [
        ['listen', '80'],
        ['server_name', 'foo.com'],
        ['root', '/home/ubuntu/sites/foo/']]]]


Dumping:

    >>> from nginxparser import dumps
    >>> dumps([['server'], [
                ['listen', '80'],
                ['server_name', 'foo.com'],
                ['root', '/home/ubuntu/sites/foo/']]])

    'server {
        listen   80;
        server_name foo.com;
        root /home/ubuntu/sites/foo/;
     }'
