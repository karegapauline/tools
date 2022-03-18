---
title: Modules
subtitle: Show information about a module
---

# Show information about a module

For quick help about how a module works, use `nf-core modules info <tool>`.
This shows documentation about the module on the command line, similar to what's available on the
[nf-core website](https://nf-co.re/modules).

```console
$ nf-core modules info fastqc

                                          ,--./,-.
          ___     __   __   __   ___     /,-._.--~\
    |\ | |__  __ /  ` /  \ |__) |__         }  {
    | \| |       \__, \__/ |  \ |___     \`-._,-`-,
                                          `._,._,'

    nf-core/tools version 2.3.dev0 - https://nf-co.re


╭─ Module: fastqc  ───────────────────────────────────────────────────────────────────────────────────────╮
│ 🌐 Repository: nf-core/modules                                                                          │
│ 🔧 Tools: fastqc                                                                                        │
│ 📖 Description: Run FastQC on sequenced reads                                                           │
╰─────────────────────────────────────────────────────────────────────────────────────────────────────────╯
               ╷                                                                                  ╷
 📥 Inputs     │Description                                                                       │Pattern
╺━━━━━━━━━━━━━━┿━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┿━━━━━━━╸
  meta  (map)  │Groovy Map containing sample information e.g. [ id:'test', single_end:false ]     │
╶──────────────┼──────────────────────────────────────────────────────────────────────────────────┼───────╴
  reads  (file)│List of input FastQ files of size 1 and 2 for single-end and paired-end data,     │
               │respectively.                                                                     │
               ╵                                                                                  ╵
                  ╷                                                                       ╷
 📤 Outputs       │Description                                                            │        Pattern
╺━━━━━━━━━━━━━━━━━┿━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┿━━━━━━━━━━━━━━━╸
  meta  (map)     │Groovy Map containing sample information e.g. [ id:'test',             │
                  │single_end:false ]                                                     │
╶─────────────────┼───────────────────────────────────────────────────────────────────────┼───────────────╴
  html  (file)    │FastQC report                                                          │*_{fastqc.html}
╶─────────────────┼───────────────────────────────────────────────────────────────────────┼───────────────╴
  zip  (file)     │FastQC report archive                                                  │ *_{fastqc.zip}
╶─────────────────┼───────────────────────────────────────────────────────────────────────┼───────────────╴
  versions  (file)│File containing software versions                                      │   versions.yml
                  ╵                                                                       ╵

 💻  Installation command: nf-core modules install fastqc

```
