# Anti-Debug Tricks

### Description

Debugging is the essential part of malware analysis. Every time when we need to go deep down to malware behavior, restore encryption methods or examine communication protocols – generally, all the time we need to examine memory in a certain moment of time – we use debuggers.

Debuggers interfere with the debugging process such a way that usually produces side-effects. These side-effects often checked by malicious programs to verify if it is executed under debugging. Knowledge of anti-debug techniques helps us to detect when the malware tries to prevent us debugging it and mitigate the interference in due course.

The encyclopedia contains the description of anti-debug tricks which work on latest Windows releases with the most popular debuggers (such as OllyDbg, WinDbg, x64dbg). Deprecated techniques (e.g. for SoftICE, etc.) are not included in our encyclopedia (despite all the love to SoftICE).

Anti-Debug tricks grouped d by the way which triggers side-effects (“meh, yet another classification”, you might think). Each group includes the description of corresponding tricks, their implementation in C/C++ or x86/x86-64 Assembly language and recommendations how to mitigate the described trick for developers who want to create anti-anti-debug solution. But, in general, for bypassing anti-debug techniques we recommend using [ScyllaHide][scylla_link] plugin which supports OllyDbg, x64dbg and IDA Pro.

All the techniques which are described in this encyclopedia are implemented in our [ShowStopper][showstopper_link] open-source project. It can help you to better understand how these techniques work or to assess the debuggers and anti-anti-debug plugins.

<div style="text-align: right">
    Yaraslau Harakhavik,<br />
    <i>Reverse Engineer at Check Point Research</i>
</div>
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
