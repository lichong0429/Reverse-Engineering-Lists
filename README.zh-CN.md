# 逆向工程资源清单（中文版）

> 一份精选的**逆向工程（Reverse Engineering）**学习与工具资源清单，覆盖书籍、课程、练习靶场、十六进制编辑器、二进制格式、反汇编器、动态分析、调试器、脚本化、Android、YARA 等方向。
>
> 本仓库 fork 自 **[wtsxDev/reverse-engineering](https://github.com/wtsxDev/reverse-engineering)**；英文原版清单见 **[README.md](README.md)**，中文翻译与说明由仓库维护者补充。

[![Awesome](https://2.bp.blogspot.com/-nz0jFFFA4Hc/WHubiaz8ecI/AAAAAAAAB08/g2erX6roVBYCfwWjIGUOBYMkcB7ghRL2wCLcB/s1600/reverse%2Bengineering.png)](http://kalitut.com)

---

## 目录

| 分类 | 内容 |
|---|---|
| [书籍 Books](#书籍-books) | 逆向、恶意代码分析、内存取证、Windows 内核等经典教材 |
| [课程 Courses](#课程-courses) | 免费/付费系统课程与培训（OpenSecurityTraining、RPISEC 等） |
| [练习靶场 Practice](#练习靶场-practice) | CrackMe、CTF、恶意样本库（**注意安全**） |
| [十六进制编辑器 Hex Editors](#十六进制编辑器-hex-editors) | 二进制/十六进制查看与编辑 |
| [二进制格式 Binary Format](#二进制格式-binary-format) | PE / Mach-O 结构解析工具 |
| [反汇编器 Disassemblers](#反汇编器-disassemblers) | IDA、Ghidra、Binary Ninja、Radare2 等 |
| [二进制分析 Binary Analysis](#二进制分析-binary-analysis) | 符号执行、二进制平台、SMT 求解 |
| [字节码分析 Bytecode Analysis](#字节码分析-bytecode-analysis) | .NET / Java / Flash 反编译 |
| [导入表重建 Import Reconstruction](#导入表重建-import-reconstruction) | 脱壳后修复导入表 |
| [动态分析 Dynamic Analysis](#动态分析-dynamic-analysis) | 进程/网络/文件行为监控与内存取证 |
| [调试器 Debugging](#调试器-debugging) | 用户态与内核态调试 |
| [Mac 解密 Mac Decrypt](#mac-解密-mac-decrypt) | macOS 应用解密与 dump |
| [文档分析 Document Analysis](#文档分析-document-analysis) | Office / PDF 恶意文档分析 |
| [脚本化 Scripting](#脚本化-scripting) | IDAPython、PE 解析等自动化 |
| [Android](#android) | APK 反编译与逆向工具链 |
| [YARA](#yara) | 恶意样本特征规则 |

---

## 使用说明

1. **按阶段取用**：入门先看「书籍 + 课程」，再上「练习靶场」，然后按分析类型挑工具。
2. **工具无需全装**：实战常用的组合见文末[「推荐工具链速查」](#推荐工具链速查)。
3. **⚠️ 安全提醒**：练习区包含真实恶意样本下载源，**务必在隔离虚拟机 / 专用测试机中操作**，不要在主力机运行任何样本。

---

## 书籍 Books

*逆向工程经典教材（英文原版）*

* [The IDA Pro Book](http://amzn.to/2jTicOg)
* [Radare2 Book](https://www.gitbook.com/book/radare/radare2book/details)
* [Reverse Engineering for Beginners](http://beginners.re/) —— 免费电子书，入门首选
* [The Art of Assembly Language](http://amzn.to/2jlxTNp)
* [Practical Reverse Engineering](http://amzn.to/2iusXRW)
* [Reversing: Secrets of Reverse Engineering](http://amzn.to/2jlnBwX)
* [Practical Malware Analysis](http://amzn.to/2jljYqE) —— 恶意代码分析标准教材
* [Malware Analyst's Cookbook](http://amzn.to/2iWPJDd)
* [Gray Hat Hacking](http://amzn.to/2jllIAi)
* [Access Denied](https://github.com/shaykhsiddique/academic-/blob/master/CSE107/Access%20Denied.pdf)
* [The Art of Memory Forensics](http://amzn.to/2jMJQs0)
* [Hacking: The Art of Exploitation](http://amzn.to/2jnkV19)
* [Fuzzing for Software Security](http://amzn.to/2jMKCWc)
* [Art of Software Security Assessment](http://amzn.to/2jlvtyt)
* [The Antivirus Hacker's Handbook](http://amzn.to/2jn9G99)
* [The Rootkit Arsenal](http://amzn.to/2jlgioK)
* [Windows Internals Part 1](http://amzn.to/2jlo9mA) · [Part 2](http://amzn.to/2jMLCth)
* [Inside Windows Debugging](http://amzn.to/2iqFTxf)
* [iOS Reverse Engineering](https://github.com/iosre/iOSAppReverseEngineering)

## 课程 Courses

*系统性逆向 / 恶意分析课程与培训*

* [Lenas Reversing for Newbies](https://tuts4you.com/download.php?list.17)
* [Open Security Training](http://opensecuritytraining.info/Training.html) —— 免费，体系完整
* [Dr. Fu's Malware Analysis](http://fumalwareanalysis.blogspot.sg/p/malware-analysis-tutorials-reverse.html)
* [Binary Auditing Course](http://www.binary-auditing.com/)
* [TiGa's Video Tutorials](http://www.woodmann.com/TiGa/)
* [Legend of Random](https://tuts4you.com/download.php?list.97)
* [Modern Binary Exploitation](http://security.cs.rpi.edu/courses/binexp-spring2015/)
* [RPISEC Malware Course](https://github.com/RPISEC/Malware)
* [SANS FOR 610 GREM](https://www.sans.org/course/reverse-engineering-malware-malware-analysis-tools-techniques/Type/asc/all)
* [REcon Training](https://recon.cx/2015/training.html)
* [Blackhat Training](https://www.blackhat.com/us-16/training/)
* [Offensive Security](https://www.offensive-security.com/information-security-training/)
* [Corelan Training](https://www.corelan.be/index.php/articles/#cat_exploit-writing-tutorials)
* [Offensive and Defensive Android Reversing](https://github.com/rednaga/training/raw/master/DEFCON23/O%26D%20-%20Android%20Reverse%20Engineering.pdf)

## 练习靶场 Practice

*⚠️ 该分类含恶意样本源，请在隔离环境中使用*

* [Crackmes.de](http://www.crackmes.de/)
* [OSX Crackmes](https://reverse.put.as/crackmes/)
* [ESET Challenges](http://www.joineset.com/jobs-analyst.html)
* [Flare-on Challenges](http://flare-on.com/) —— 年度逆向挑战赛
* [Github CTF Archives](http://github.com/ctfs/)
* [Reverse Engineering Challenges](http://challenges.re/)
* [xorpd Advanced Assembly Exercises](http://www.xorpd.net/pages/xchg_rax/snip_00.html)
* [Virusshare.com](http://virusshare.com/)
* [Contagio](http://contagiodump.blogspot.com/)
* [Malware-Traffic-Analysis](https://malware-traffic-analysis.com/)
* [Malshare](http://malshare.com/)
* [Malware Blacklist](http://www.malwareblacklist.com/showMDL.php)
* [malwr.com](https://malwr.com/)
* [vxvault](http://vxvault.net/)

## 十六进制编辑器 Hex Editors

*二进制查看与编辑*

* [HxD](https://mh-nexus.de/en/hxd/) —— Windows 上最常用的免费十六进制编辑器
* [010 Editor](http://www.sweetscape.com/010editor/) —— 支持模板脚本解析文件结构
* [Hex Workshop](http://www.hexworkshop.com/)
* [HexFiend](http://ridiculousfish.com/hexfiend/) —— macOS
* [Hiew](http://www.hiew.ru/) —— 老牌二进制编辑器，内置反汇编
* [hecate](https://github.com/evanmiller/hecate)

## 二进制格式 Binary Format

*PE / Mach-O 等可执行文件结构解析*

* [CFF Explorer](http://www.ntcore.com/exsuite.php)
* [Cerbero Profiler](http://cerbero.io/profiler/) · [Lite PE Insider](http://cerbero.io/peinsider/)
* [Detect It Easy](http://ntinfo.biz/) —— 查壳 / 编译器指纹识别
* [PeStudio](http://www.winitor.com/) —— 静态快速筛查
* [PEiD](https://tuts4you.com/download.php?view.398)
* [MachoView](https://github.com/gdbinit/MachOView)
* `nm` —— 查看符号表（[man](https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man1/nm.1.html)）
* `file` —— 识别文件类型（[man](https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man1/file.1.html)）
* `codesign` —— 查看代码签名信息，用法：`codesign -dvvv 文件名`（[man](https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man1/codesign.1.html)）

## 反汇编器 Disassemblers

*静态反汇编引擎与平台*

* [IDA Pro](https://www.hex-rays.com/products/ida/index.shtml) —— 业界标准（商业）
* [GHIDRA](https://ghidra-sre.org/) —— NSA 开源反汇编/反编译套件
* [Binary Ninja](https://binary.ninja/) —— 现代商业逆向平台，API 友好
* [Radare](http://www.radare.org/r/) —— 开源，命令行驱动
* [Hopper](http://hopperapp.com/) —— macOS / Linux
* [Capstone](http://www.capstone-engine.org/) —— 反汇编框架（可嵌入自己程序）
* [objdump](http://linux.die.net/man/1/objdump) —— GNU binutils
* [fREedom](https://github.com/cseagle/fREedom)

## 二进制分析 Binary Analysis

*符号执行、二进制分析平台、SMT 求解*

* [Mobius Resources](http://www.msreverseengineering.com/research/)
* [z3](https://z3.codeplex.com/) —— SMT 求解器
* [bap](https://github.com/BinaryAnalysisPlatform/bap) —— Binary Analysis Platform
* [angr](https://github.com/angr/angr) —— 符号执行框架，常用于自动化漏洞挖掘

## 字节码分析 Bytecode Analysis

*.NET / Java / Flash 反编译*

* [dnSpy](https://github.com/0xd4d/dnSpy) —— .NET 调试与反编译
* [Bytecode Viewer](https://bytecodeviewer.com/) —— Java 多反编译器集成
* [Bytecode Visualizer](http://www.drgarbage.com/bytecode-visualizer/)
* [JPEXS Flash Decompiler](https://www.free-decompiler.com/flash/)

## 导入表重建 Import Reconstruction

*脱壳后修复被破坏的导入表*

* [ImpRec](http://www.woodmann.com/collaborative/tools/index.php/ImpREC)
* [Scylla](https://github.com/NtQuery/Scylla) —— x64 兼容，目前主流选择
* [LordPE](http://www.woodmann.com/collaborative/tools/images/Bin_LordPE_2010-6-29_3.9_LordPE_1.41_Deluxe_b.zip)

## 动态分析 Dynamic Analysis

*进程 / 网络 / 文件行为监控与内存取证*

* [ProcessHacker](http://processhacker.sourceforge.net/) —— 增强版任务管理器
* [Process Explorer](https://technet.microsoft.com/en-us/sysinternals/processexplorer)
* [Process Monitor](https://technet.microsoft.com/en-us/sysinternals/processmonitor) —— 文件/注册表/进程实时监控
* [Autoruns](https://technet.microsoft.com/en-us/sysinternals/bb963902)
* [Noriben](https://github.com/Rurik/Noriben) —— Procmon 自动化分析脚本
* [API Monitor](http://www.rohitab.com/apimonitor)
* [iNetSim](http://www.inetsim.org/) —— 网络模拟
* [SmartSniff](http://www.nirsoft.net/utils/smsniff.html)
* [TCPView](https://docs.microsoft.com/en-us/sysinternals/downloads/tcpview)
* [Wireshark](https://www.wireshark.org/download.html)
* [Fakenet](http://practicalmalwareanalysis.com/fakenet/)
* [Volatility](https://github.com/volatilityfoundation/volatility) —— 内存取证框架
* [Dumpit](http://www.moonsols.com/products/) —— 内存镜像抓取
* [LiME](https://github.com/504ensicsLabs/LiME) —— Linux 内存提取
* [Cuckoo](https://www.cuckoosandbox.org/) —— 开源自动化沙箱
* [Objective-See Utilities](https://objective-see.com/products.html) —— macOS 安全工具集
* [XCode Instruments](https://developer.apple.com/xcode/download/) —— 监控文件与进程（[用户指南](https://developer.apple.com/library/watchos/documentation/DeveloperTools/Conceptual/InstrumentsUserGuide/index.html)）
* [dtrace](http://dtrace.org/blogs/brendan/2011/10/10/top-10-dtrace-scripts-for-mac-os-x/) —— `sudo dtruss` 相当于 `strace`（[dtrace recipes](http://mfukar.github.io/2014/03/19/dtrace.html)）
* [fs_usage](https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man1/fs_usage.1.html) —— 实时报告文件系统相关系统调用与缺页；文件 I/O：`fs_usage -w -f filesystem`
* [dmesg](https://developer.apple.com/library/mac/documentation/Darwin/Reference/ManPages/man8/dmesg.8.html) —— 显示系统消息缓冲区

## 调试器 Debugging

*用户态 / 内核态调试*

* [WinDbg](https://msdn.microsoft.com/en-us/windows/hardware/hh852365.aspx) —— Windows 内核调试首选
* [OllyDbg v1.10](http://www.ollydbg.de/) · [v2.01](http://www.ollydbg.de/version2.html) —— 经典 32 位调试器
* [OllySnD](https://tuts4you.com/download.php?view.2061) · [Olly Shadow](https://tuts4you.com/download.php?view.6) · [Olly CiMs](https://tuts4you.com/download.php?view.1206) · [Olly UST_2bg](https://tuts4you.com/download.php?view.1206) —— OllyDbg 增强插件
* [x64dbg](http://x64dbg.com/#start) —— 开源 x64/x32 调试器，现代替代方案
* [gdb](https://www.gnu.org/software/gdb/) —— GNU 调试器
* [vdb](https://github.com/vivisect/vivisect)
* [lldb](http://lldb.llvm.org/)
* [qira](http://qira.me/)
* [unicorn](https://github.com/unicorn-engine/unicorn) —— CPU 模拟框架

## Mac 解密 Mac Decrypt

*macOS 应用解密与进程 dump*

* [Cerbero Profiler](http://cerbero-blog.com/?p=1311) —— 全选 → 复制到新文件
* [AppEncryptor](https://github.com/AlanQuatermain/appencryptor) —— 解密工具
* [Class-Dump](http://stevenygard.com/projects/class-dump/) —— 使用 deprotect 选项
* [readmem](https://github.com/gdbinit/readmem) —— OS X 进程 dump 工具

## 文档分析 Document Analysis

*Office / PDF 恶意文档分析*

* [Ole Tools](http://www.decalage.info/python/oletools) —— OLE / VBA 宏分析
* [Didier's PDF Tools](http://blog.didierstevens.com/programs/pdf-tools/)
* [Origami](https://github.com/cogent/origami-pdf)

## 脚本化 Scripting

*IDAPython 与自动化分析*

* [IDA Python Src](https://github.com/idapython/src)
* [IDC Functions Doc](https://www.hex-rays.com/products/ida/support/idadoc/162.shtml)
* [Using IDAPython to Make your Life Easier](http://researchcenter.paloaltonetworks.com/tag/idapython/)
* [Introduction to IDA Python](https://tuts4you.com/download.php?view.3229)
* [The Beginner's Guide to IDA Python](https://leanpub.com/IDAPython-Book)
* [IDA Plugin Contest](https://www.hex-rays.com/contests/)
* [onehawt IDA Plugin List](https://github.com/onethawt/idaplugins-list)
* [pefile Python Library](https://github.com/erocarrera/pefile) —— Python 解析 PE 文件

## Android

*APK 反编译与逆向工具链*

* [Android Studio](http://developer.android.com/sdk/index.html)
* [APKtool](http://ibotpeaches.github.io/Apktool/) —— APK 解包/重打包
* [dex2jar](https://github.com/pxb1988/dex2jar)
* [Bytecode Viewer](https://bytecodeviewer.com/)
* [IDA Pro](https://www.hex-rays.com/products/ida/index.shtml)
* [JaDx](https://github.com/skylot/jadx) —— Dex → Java 反编译

## YARA

*恶意样本特征规则编写*

* [Yara docs](http://yara.readthedocs.org/en/v3.4.0/writingrules.html)
* [Cheatsheet](https://gist.github.com/0xtyh/eeabc765e9befad9b80a)
* [yarGen](https://github.com/Neo23x0/yarGen) —— 规则自动生成
* [Yara First Presentation](https://www.first.org/resources/papers/conference2014/first_2014_-_schuster-_andreas_-_yara_basic_and_advanced_20140619.pdf)

---

## 推荐工具链速查

按分析任务选择，避免装一堆重复工具：

| 分析任务 | 推荐组合 |
|---|---|
| **静态反汇编 / 反编译** | Ghidra（免费）或 IDA Pro（商业）+ Detect It Easy 查壳 |
| **Windows 用户态动态调试** | x64dbg（开源）+ API Monitor（看 API 调用） |
| **Windows 内核调试** | WinDbg + Windows Internals 教材 |
| **行为监控** | Process Monitor + Process Explorer + Noriben（自动化） |
| **网络行为** | Wireshark + FakeNet-NG / INetSim |
| **自动化沙箱分析** | Cuckoo Sandbox |
| **内存取证** | Volatility（+ DumpIt / LiME 抓镜像） |
| **Android** | jadx + apktool（+ Frida 做运行时插桩） |
| **脚本化批量处理** | IDAPython / Ghidra Script + pefile |
| **样本规则化检测** | YARA + yarGen |

---

## 延伸阅读

原清单附带的相关书单（kalitut）：

* [Top Hacking Books](http://www.kalitut.com/2016/12/best-ethical-hacking-books.html)
* [Top Reverse Engineering Books](http://www.kalitut.com/2017/01/Best-reverse-engineering-books.html)
* [Top Machine learning Books](http://www.kalitut.com/2017/01/machine-learning-book.html)
* [Top 5 books Programming Books](http://www.kalitut.com/2017/01/Top-Programming-Books.html)
* [Top Java Books](http://www.kalitut.com/2017/01/Best-Java-Programming-Books.html)

---

## 免责声明

本清单仅为资源索引，所链接的第三方工具、课程与**恶意样本下载源**均不由本仓库提供或担保。
使用样本、靶场与相关工具时，**请在隔离环境（虚拟机 / 独立测试机）中进行**，并遵守当地法律法规；
不得将相关技术用于任何未授权的系统。

---

## 致谢与许可

- **原始清单**：[wtsxDev/reverse-engineering](https://github.com/wtsxDev/reverse-engineering)（本仓库为其 fork）
- 原清单封面图来源：[kalitut.com](http://kalitut.com)
- 本仓库**未声明开源许可证**，版权归原作者所有；本文件仅为中文翻译与整理，便于中文使用者查阅。
