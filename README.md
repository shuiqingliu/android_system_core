
The system/ directory is intended for pieces of the world that are the
core of the embedded linux platform at the heart of Android.  These
essential bits are required for basic booting, operation, and debugging.

They should not depend on libraries outside of system/... (some of them
do currently -- they need to be updated or changed) and they should not
be required for the simulator build.

The license for all these pieces should be clean (Apache2, BSD, or MIT).

Currently system/bluetooth/... and system/extra/... have some pieces
with GPL/LGPL licensed code.

Assorted Issues:

- pppd depends on libutils for logging
- pppd depends on libcrypt/libcrypto
- init, linker, debuggerd, toolbox, usbd depend on libcutils
- should probably rename bionic to libc


-test
    {
        "server":"my_server_ip",
        "server_port":8388,
        "local_address": "127.0.0.1",
        "local_port":1080,
        "password":"mypassword",
        "timeout":300,
        "method":"aes-256-cfb",
        "fast_open": false
    }
