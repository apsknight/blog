---
layout: post
title:  "Setting up Competitive Programming Environment"
date:   2017-06-25 13:00:00 +0530
categories: sublime ubuntu coding cloud9 pastebin
comments: true
---
![](http://www.geeksforgeeks.org/wp-content/uploads/Competitive-Programming.jpg)

This blog post emphasize some random *Gyan* which may be useful for competitive programmerss during coding contests.

## 1. Chosing an Operating System
Almost every beginner use Windows but the OS preferred by veteran developers and programmers is certainly Linux as it provide a better coding experience and plethora of customization opportunities.

The following article describe why you should consider using Linux:   
[7 Superb Reasons Why You Should Use Linux For Programming](http://www.makeuseof.com/tag/6-superb-reasons-use-linux-programming/)

### Chosing a Linux Distro
The another great thing about Linux is that there are plenty of distros available. Few popular distros are:  
* Ubuntu
* Fedora
* CentOS
* Mint
* openSUSE

I personally work on Ubuntu as it is one of the most popular distro with awesome community support and its package manager library **apt** and **dpkg** have almost all requisite packages for a good coding setup. You can chose any distro as they are almost similar to each other.


If you don't want to miss the awesome graphical aesthetics of Windows, Linux can be dual booted alongwith Windows (I prefer this way): [Dual booting windows with Ubuntu](http://www.everydaylinuxuser.com/2015/11/how-to-install-ubuntu-linux-alongside.html)


### Simplify your life by **Bash**ing
The most useful tool offered by UNIX like operating system is BASH. Yeah, the same prompting green shell that Hackers use in hollywood movies. The basic commands like `cd, ls, mkdir, rm, chmod` are quite handy while interacting with FHS.  
It is advised to learn basic Linux shell commands before proceeding. You can enroll in this free introductory course offered by **The Linux Foundation** on [edX](https://www.edx.org/course/introduction-linux-linuxfoundationx-lfs101x-1).

### Useful Linux Packages
* **Git**  
It is a version controlling system build by Linux founder *Linus Torvalds*. You can learn it in just 15 minutes [here](https://try.github.io/levels/1/challenges/1). Execute the following code in terminal to install git (for Ubuntu):
```bash
sudo apt-get update
sudo apt-get install git
```
Configure git:
```bash
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

* **Google Chrome**  
No need to say anything on this. Here is the command to install:
```bash
sudo apt-get install libxss1 libappindicator1 libindicator7
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo dpkg -i google-chrome*.deb
```
* **VLC Media Player**  
Again, no need to say anything. Here is the command to install:
```bash
sudo apt-get update
sudo apt-get install vlc browser-plugin-vlc
```
* **MacBuntu**  
Intrested in customizing your ubuntu to display like a MacBook? for eg. Following is the screenshot of my Desktop:  
![](https://image.ibb.co/hzYMQ5/Screenshot_from_2017_06_25_14_49_08.png)
[This is the link of MacBuntu installation guide.](http://www.noobslab.com/2016/04/macbuntu-1604-transformation-pack-for.html)

___


## 2. Chosing a Programming Language
The most important weapon for a competitive programmer is Programming language. You can do competitive programming in almost any language but the language preferred by most of the programmers is **C++** followed by **Java** and **Python**. ACM ICPC allows only 4 languages (C/C++, Java and Python) in world finals. I personally use C++ because of its awesome STL(Standard Template Library) and also it is a bit faster than Java. Java is heavily based on OOP so even writing a simple Hello World! program require many lines. Also it is very easy for C programmers to step up on C++ as C is a subset of C++. Using C++ is advisable alongwith basic knowledge of Python as Python can be helpful while dealing with big integers. Following pie chart shows the most used programming language on [Hackerearth](http://www.hackerearth.com) online judge.
![](http://i2.wp.com/blog.hackerearth.com/wp-content/uploads/2016/11/Game_deck-18-1-1.jpg)
You can enroll in C++ course offered by **John Purcell** on [Udacity](https://www.udemy.com/free-learn-c-tutorial-beginners/) to learn basic C++ programming. However if you prefer learning from textual tutorials, <http://www.cplusplus.com/doc/tutorial/> can be useful for you.

### Few useful C++ tricks:
* **Speedify C++ I/O**  
The standard C++ I/O functions (cin/cout) flush the buffer on every next I/O call which unncecessarily increase I/O time. For enhancing C++ I/O speed, you can either use C's standard I/O function (scanf/printf) instead of (cin/cout) or you can write the following lines in main function.
```cpp
ios_base::sync_with_stdio(0);
cin.tie(0);
cout.tie(0);
```
Similarly the C++ `endl` also flush the buffer. You can either use C's `'\n'` instead of `endl` or you can write the following macro in your C++ file.
```cpp
#define endl '\n'
```

* **Get rid of those includes!**  
Simply use
```cpp
#include <bits/stdc++.h>
```
This library includes many of libraries we do need in contest like `algorithm`, `iostream`, `vector` and many more. Believe me you don't need to include anything else


___

## 3. Chosing a Text Editor
Many programmers prefer an Integrated Developement Environment(IDE) like Code::Block, DevC++, Eclipse etc. but I think using an IDE for competitive programming is an overkill. Personally for me IDEs are best suited for big developement projects, however I feel more efficient on Text Editors like Sublime Text in coding contests. Also text editors provide plethora of shortcuts like `Ctrl + D`, `Ctrl + KK`, multiple cursors etc. to make your life fast and easy. I prefer Sublime Text over Atom as Atom is built with [Electron](https://electron.atom.io/) which is powered by Chrome engine thus making Atom slow while booting. You can install Sublime Text by executing following command in your shell:
```bash
sudo add-apt-repository ppa:webupd8team/sublime-text-3
sudo apt-get update
sudo apt-get install sublime-text-installer
```
You can run sublime text either clicking its icon in search menu or by executing following command in shell:
```bash 
subl file_address.extension
```
To improve Subime Text's aesthetics, you can install themes like **Brogrammer** from **Package Control**. For that you have to first install [Package Control](https://packagecontrol.io/installation) followed by [Brogrammer](https://packagecontrol.io/packages/Theme%20-%20Brogrammer).

Screenshot of my Sublime Text:
![My Sublime Text 3](https://image.ibb.co/n5SgQ5/Screenshot_from_2017_06_25_15_40_17.png)

#### Using sublime without knowing its super useful shortcuts is futile.
You must learn useful sublime text's shortcuts to gear up your coding speed. [Click Here](https://gist.github.com/eteanga/1736542) for Sublime text shortcuts cheatsheet. Don't forget to bookmark them.

### Sublime Text Snippets feature:
Quoting from Sublime Text documentation:
>Whether you are coding or writing the next vampire best-seller, you’re likely to need certain short fragments of text again and again. Use snippets to save yourself tedious typing. Snippets are smart templates that will insert text for you and adapt it to their context.


For a C++ programmer writing macros, typedef, including libraries etc. everytime while creating a new file can be a WET practice. So to [DRY](http://softwareyoga.com/is-your-code-dry-or-wet/) up this you can use sublime snippet feature.

> To create a new snippet, select **Tools > Developer > New Snippet…**. Sublime Text will present you with skeleton for a new snippet.

Now delete everything and copy-paste the following: 
```cson
<snippet>
	<content><![CDATA[
	<!-- Your Snippet Code here -->
}
]]></content>
	<tabTrigger>code</tabTrigger>
</snippet>
```
Replace `<!-- Your Snippet Code here -->` comment with your desired snippet.
Now save the file in default directory with a name like `cpp.sublime-snippet`.


For example following is my C++ snippet code: 
```cpp
/**
*	Name: Aman Pratap Singh (@apsknight, </www.apsknight.cf>)
*	Institute: Indian Institute of Technology Bhubaneswar 
*/
#include <bits/stdc++.h>
using namespace std;

typedef long long ll;
typedef string st;
typedef vector<int> vi;
typedef vector<st> vs;
#define rep(i, n) for(int i = 0; i < n; i++)
#define fogg(i,a,b) for(int i = (a); i <= (b); i++)
#define ford(i,a,b) for(int i = (a); i >= (b); i--)
#define test int t; cin >> t; while(t--)
#define debug(x) cout << '>' << #x << ':' << x << "\n";
#define endl '\n'
#define off ios_base::sync_with_stdio(0); cin.tie(0); cout.tie(0)
#define maxx 1e6+7

int main() {
	off;
	$0

  	return 0;
}
```
For triggering this you have to just type `code + TAB` in your C++ file.
Notice the $0 sign in 2nd line of main function in my snippet. This $0 sign tells sublime to place the cursor here after triggering the snippet.

Beside this, Sublime also has plenty other useful features, to learn them you may consider downloading this [awesome book](http://nbviewer.jupyter.org/github/Kristinita/SashaBooks/blob/master/IT/Sublime%20Text/Sublime%20Text%20Power%20User.pdf) by **Wes Bos**.

You can also visit this blog for setting up sublime for your coding environment: <http://blog.codingblocks.com/2017/setting-up-sublime-text-for-competitive-coding>

#### Other Popular Text Editors:
* Vim (Most famous CLI text editor due to Large plugin support and customization)
* Emacs (Another famous CLI text editor)
* Notepad++
* Gedit (Default text editor of Ubuntu)
* Visual Studio (Famous text editor by Microsoft)

___

## 4. Other useful Gyan
Some useful things that may save your life during your proramming journey.

### Code Hosting
Suppose you stucked in an infinite loop or segmentation fault while solving a problem and you realize that your friend may help in this case. In this case sending your code to your friend on FB Messanger/Whatsapp/Hike or Emailing the code is not certainly a good idea. Here comes the sites such as pastebin, ideone which may help you by hosting the code on their server and you can share just a tiny URL to your friend.

There are quite a few such services available on Internet. Following are some of them:

* [Pastebin](https://pastebin.com/)
* [Github Gist](https://gist.github.com/)
* [IDEone](http://www.ideone.com/)
* [Fedora Pastebin](https://paste.fedoraproject.org/)
* [Paste Ubuntu](http://paste.ubuntu.com)

Personally I prefer the last one <http://paste.ubuntu.com/> because of its Gedit like Rich Synax Highlighting, nice UX and no Login/Authentication is required. Also the sharing link of Ubuntu Paste's is much shorter than other.

### Cloud9 - The next generation IDE
Cloud9 combines a powerful online code editor with a full Ubuntu workspace in the cloud. Cloud9 supports more than 40 languages. This may be useful when you have to code and you don't have your laptop around. This service provide you an IDE in your browser which require only good internet connection. It also provide many other features like workspace sharing, simultaneous coding, built-in terminal, **awesome debugger** and much more. You can create one private workspace and unlimited public workspace with a free account. For knowing more about Cloud9, Visit <https://c9.io>.

### GDB and Valgrind
GDB is a debugger built by GNU which can help you in debugging your C++ files and Valgrind is a tool which can check if there is any memory leakage in your program. For nore details about them, you can refer to these videos: 
[GDB](https://www.youtube.com/watch?v=y5JmQItfFck), 
[Valgrind](https://www.youtube.com/watch?v=fvTsFjDuag8)

### Markdown
Markdown is a markup language like HTML. Learning it may not be important but it may be useful in writing rich comments. Some online judges like **Codechef** support writing comments with markdown. Also it is an important tool while writing documentation of your code (which probably you'll never do in competitive programming). Markdown is quite useful in web development. This blog post is also written in markdown.  
You can learn basic markdown [here](http://commonmark.org/help/tutorial/), You should also bookmark [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) for your future reference.

### Shell scripting
Shell scripting can be useful for automating repetitive stuff. For eg. I created following script for my cloud9 IDE, which on executing ask for a problem code and create a new C++ file.

```bash
#!/bin/sh
# Navigate to the folder in which the file has to be created. 
echo Program Code?
# Ask for Program code.
read code
# path is variable storing absolute file path.
path=$(pwd)/$code.cpp
# touch(create) file.
touch $path
# Write default snippet in 
echo "#include <bits/stdc++.h>\nusing namespace std;\n\ntypedef long long ll;\n#define repeat(i,n) for(int i = 0; i < n; i++)\n\nint main() {\n\tios_base::sync_with_stdio(0);\n\tcin.tie(0);\n\n\treturn 0;\n}" >> $path
c9 $path
echo "Okay! Done :)"
```
You can also find this script in my [Github repository](https://github.com/apsknight/snippets/blob/master/initialize.sh).  
Visit this awesome [tutorial](https://www.shellscript.sh/) for learning shell scripting.

___

...  


Image Source: Geeksforgeeks, Hackerearth  
You can comment below any doubt / criticism or compliment. Also if you like this post please share it among your hacker friends.   
*Don’t forget to bookmark my blog and keep visiting frequently. Bonne journee!*