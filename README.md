# Anti-Debug Tricks

### Description

Debugging is the essential part of malware analysis. Every time we need to drill down into malware behavior, restore encryption methods or examine communication protocols – generally, whenever we need to examine memory at a certain moment of time – we use debuggers.

Debuggers interfere with the debugged process in a way that usually produces side-effects. These side-effects are often used by malicious programs to verify if they are executed under debugging. In turn knowledge of anti-debug techniques helps us detect when the malware tries to prevent us from debugging it and mitigate the interference.

This encyclopedia contains the description of anti-debug tricks which work on the latest Windows releases with the most popular debuggers (such as OllyDbg, WinDbg, x64dbg). Deprecated techniques (e.g. for SoftICE, etc.) are not included (despite all the love to SoftICE).

Anti-Debug tricks are grouped by the way in which they trigger side-effects (“meh, yet another classification”, you might think). Each group includes the description of corresponding tricks, their implementation in C/C++ or x86/x86-64 Assembly language, and recommendations of how to mitigate the trick for developers who want to create their own anti-anti-debug solution. In general, for bypassing anti-debug techniques we recommend using the [ScyllaHide][scylla_link] plugin which supports OllyDbg, x64dbg and IDA Pro.

All the techniques which are described in this encyclopedia are implemented in our [ShowStopper][showstopper_link] open-source project. The encyclopedia can help you to better understand how these techniques work or to assess debuggers and anti-anti-debug plugins.

<p align="right">
    Yaraslau Harakhavik,<br />
    <i>Reverse Engineer at Check Point Research</i>
</p>
<br />

## References
* [P. Ferrie. The “Ultimate”Anti-Debugging Reference][ferrie]
* [N. Falliere. Windows Anti-Debug Reference][falliere]
* [J. Jackson. An Anti-Reverse Engineering Guide][jackson]
* [Anti Debugging Protection Techniques with Examples][apriorit]
* [simpliFiRE.AntiRE][simplifire]

[ferrie]: <http://pferrie.host22.com/papers/antidebug.pdf>
[falliere]: <https://www.symantec.com/connect/articles/windows-anti-debug-reference>
[jackson]: <https://tuts4you.com/download/2516/>
[apriorit]: <https://www.apriorit.com/dev-blog/367-anti-reverse-engineering-protection-techniques-to-use-before-releasing-software>
[simplifire]: <https://bitbucket.org/fkie_cd_dare/simplifire.antire/src/master/>

[scylla_link]: <https://github.com/x64dbg/ScyllaHide>
[showstopper_link]: <https://github.com/CheckPointSW/showstopper>
