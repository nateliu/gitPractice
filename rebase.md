I want to use git rebase -i git_guid

but I am not sure how to works, so I creat this practice to test it.


step 2, I modify the rebase.md file. and I foud the first step of the submmit git_guid is: 
commit 4cec2c76624994a51484e79c442973193255cbb3
Author: Nate Liu <jinliangliu@163.com>
Date:   Mon Mar 27 21:29:04 2017 +0800

    first step: create README.md and rebase.md

step 3, modify it again.
and the step 2's commit is:
commit 549a450229425c719829c3b0f46dcc83dd1a4548
Author: Nate Liu <jinliangliu@163.com>
Date:   Mon Mar 27 21:35:57 2017 +0800

    second step : modify the rebase.md


step fourth
now I have had three steps in previous
I want combinate the latest two commit as one commit. what can i do?
1, git log, it will show the whole three git commit git_guid
2, git rebase -i 4cec2c76624994a51484e79c442973193255cbb3(it is same to git rebase -i HEAD~~ in this situation)
and the git log will asc order in the vi editor, it mean the latest step was stay in the buttom
3, change the verb pick to s for 'third step: modify rebase.md again'

4, save and input new commit message.
let type 'modify rebase.md file, it was combination by two commits' as commit message.

5, after finished rebase, use git log to see the change
commit 3829d237e838861194dfa4121f2e4689d8fde2ac
Author: Nate Liu <jinliangliu@163.com>
Date:   Mon Mar 27 21:35:57 2017 +0800

    modify the rebase.md file,it was combination by two commit.

commit 4cec2c76624994a51484e79c442973193255cbb3
Author: Nate Liu <jinliangliu@163.com>
Date:   Mon Mar 27 21:29:04 2017 +0800

    first step: create README.md and rebase.md

6, that is the rebase command. it is very userful when you're not push into remote branch. 



