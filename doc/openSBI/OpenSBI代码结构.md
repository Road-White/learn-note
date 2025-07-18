OpenSBI的完整代码结构如下:</br>
```
.
├── docs                              // 帮助文档，通过make docs生成LaTeX、html、pdf格式。
├── firmware                          // OpenSBI启动汇编以及连接脚本等。
│   ├── external_deps.mk
│   ├── fw_base.ldS
│   ├── fw_base.S
│   ├── fw_dynamic.elf.ldS
│   ├── fw_dynamic.S
│   ├── fw_jump.elf.ldS
│   ├── fw_jump.S
│   ├── fw_payload.elf.ldS
│   ├── fw_payload.S
│   ├── Kconfig
│   ├── objects.mk
│   └── payloads
├── include                           // 头文件。
├── lib
│   ├── sbi                           // 输出平台无关的libsbi.a库文件。
│   └── utils                         // 参与输出平台相关的libplatsbi.a文件。
├── Makefile
├── platform                          // 不同平台差异部分。
│   ├── fpga
│   ├── generic
│   ├── kendryte
│   ├── nuclei
│   └── template
├── README.md
├── scripts
│   ├── carray.sh
│   ├── create-binary-archive.sh
│   ├── d2c.sh
│   └── Kconfiglib
└── ThirdPartyNotices.md