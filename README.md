# mcpp
VS2012 port of the mcpp C pre-processor (http://mcpp.sourceforge.net)

Used for gcc style dependency generation on Windows.

Sample command line for .cpp code is:

```
R:\src\http\server>mcpp -+ -I../include -I../../include -D_MSC_VER -D_UNICODE -D_WINDOWS_ -MF s.dep server.cpp -o server.i
```

The resulting .dep file should contain something similar to this:

```
server.obj: R:/src/http/server/server.cpp R:/src/include/paths.h \
  R:/src/include/utils.h R:/src/include/wsinit.h R:/src/include/tsq.h \
  R:/src/include/shared.h R:/src/include/http/http_req.h \
  R:/src/include/base64.h R:/src/include/http/wsclient.h \
  R:/src/include/sha1v2.h R:/src/include/http/ws_bits.h \
  R:/src/include/http/http_ds.h
```
