# Comparison of STAC validators

There are - as far as I know - three maintained validators available for STAC:

1. The original [Python validator](https://github.com/sparkgeo/stac-validator)
3. The validation functionality shipped with [PySTAC](https://github.com/stac-utils/pystac)
4. [This Node/JavaScript validator](https://github.com/m-mohr/stac-node-validator)

Additionally I found some tools that seem to be unmaintained: [1](https://github.com/brianbancroft/stac-validator-cli) [2](https://github.com/JamesOConnor/stac-validator)

Here I'd like to give an overview of what the validators are capable of and what they are missing so that you can make a well-informed choice.

## Environment

|                            | Python Validator                           | PySTAC              | STAC Node Validator |
| :------------------------- | ------------------------------------------ | ------------------- | ------------------- |
| Validator Version          | 1.0.1                                      | 0.5.2               | 0.4.2               |
| Language                   | Python 3.6                                 | Python 3            | NodeJS              |
| CLI                        | Yes                                        | No                  | Yes                 |
| Programmatic               | Yes                                        | Yes                 | Planned             |
| Online                     | Yes, [staclint.com](https://staclint.com/) | No                  | Planned             |
| Protocols supported (Read) | HTTP(S), Filesystem                        | HTTP(S), Filesystem | HTTP(S), Filesystem |
| Gives                      | HTML / CLI / Python Output                 | Python Dict         | CLI output          |

## Specifications supported

|                                                     | Python Validator    | PySTAC              | STAC Node Validator                         |
| --------------------------------------------------- | ------------------- | ------------------- | ------------------------------------------- |
| STAC Versions supported                             | >= 0.4.0            | >= 0.4.0            | >= 1.0.0-beta.1                             |
| Protocols supported                                 | HTTP(S), Filesystem | HTTP(S), Filesystem | HTTP(S), Filesystem                         |
| Validates Items / Catalogs / Collections            | Yes                 | Yes                 | Yes                                         |
| Validates Core Extensions                           | Yes                 | Yes                 | Yes                                         |
| Validates External / Custom Extensions              | Yes                 | No                  | Yes                                         |
| Validates STAC API responses                        | No                  | No                  | Partially (only items/collections in lists) |
| Validates STAC API extensions                       | No                  | No                  | No                                          |
| Validates additional properties in STAC Item Assets | No                  | No                  | No                                          |

## Other Features

|                                | Python Validator       | PySTAC                                            | STAC Node Validator |
| :----------------------------- | ---------------------- | ------------------------------------------------- | ------------------- |
| Can follow links               | Yes                    | Yes                                               | No                  |
| Parallelisation                | Yes                    | No                                                | No                  |
| Validate against local schemas | Yes                    | Planned                                           | Yes                 |
| Other comments                 | Uses pystac validation | General Python library to work with STAC catalogs | -                   |
