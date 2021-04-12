# Analyse your HTTP response headers

This is a fork of https://github.com/marcuslindblom/security-headers using cURL natively.

Quickly and easily assess the security of your HTTP response headers using using securityheaders.com

A simple example:

```yml
on:
  deployment_status

jobs:
  security-headers-check:
    name: Analyse HTTP response headers
    runs-on: ubuntu-latest    
    steps:
      - uses: actions/checkout@v2
        with:
          repository: marcuslindblom/security-headers
      - uses: marcuslindblom/security-headers@main
        with:
          url: ${{ secrets.SECURITY_HEADERS_URL }}
          grade: A
```
