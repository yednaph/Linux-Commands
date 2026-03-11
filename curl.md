<b> Some example usage of `curl` command </b>

To download a file from a URL: `curl <url>`

To download and rename a file: `curl <url> -o <outfilename>`

To download multiple files: `curl -O <url> -O <url>`

To download a file and pass HTTP authentication: `curl -u <username>:<password> <url>`

To download a file with a proxy: `curl -x <proxy-host>:<port> <url>`

To download a file over FTP: `curl -u <username>:<password> -O ftp://ftpaddress/filename.zip`

To get an FTP directory listing: `curl ftp://username:password@example.com`

To resume a previously failed download: `curl -C - -o <partial-file> <url>`

To get your global IP: `curl httpbin.org/ip`
