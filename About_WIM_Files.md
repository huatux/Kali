###DISM Linux下的实现
```bash
apt install wimtools
```

|            命令                  |             用途                                                                        |
|---------------------------------|------------------------------------------------------------------------------------------|
|wimlib-imagex                    |解压,创建,修改,或者挂载WIM归档文件（Extract, create, modify, or mount a WIM archive）          |
|wimcapture  wimappend            |捕获或者往WIM归档中追加文件（Capture or append a WIM image）                                  |              
|wimapply                         |同DISM Apply（Apply a WIM image）                                                          |
|wimdelete                        |从WIM归档文件中删除一个镜像(Delete an image from a WIM archive)                               |
|wimexport                         |从WIM归档文件中导出镜像(Export image(s) from a WIM archive)                                 |
|wimextract                        |解压WIM镜像中的文件(Extract files from a WIM image)                                        |
|wimdir                            |列出(List the files contained in a WIM image)                                            |
|wiminfo                           |显示或修改关于WIM文件或镜像信息（Display or change information about a WIM file or image）    |
|wimjoin                           |把分离的WIM合并入一个独立的WIM（Join a split WIM into a standalone WIM）                     |
|wimmount  wimmountrw  wimunmount   | 挂载卸载WIM镜像(Mount or unmount a WIM image)                                             |
|wimoptimize                       | 优化（Optimize a WIM archive）                                                           |
|wimsplit                          |把一个WIM分离成多份（Split a WIM archive into multiple parts）                              |
|wimverify                         |校验WIM归档（Verify a WIM archive）                                                       |

