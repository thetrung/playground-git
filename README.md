## QUICK NOTE


1. Reset all un-pushed commits 

        git reset --hard @{u}
      
2. See all git commit in short form

        git log --oneline
      
      
3. Merge N-commits into one or re-arrange them :

        git rebase -i HEAD~N
        
- Merge with 1st commit :

        git rebase -i --root master
        
        
4. Force delete pushed commits :

        git push -u -f origin <commit>:dev

5. Resolve file mode changes, when you see :

        old mode 100755  
        new mode 100644  

- Use this :

        git config core.filemode false

6. Update/Merge one branch from another

        git checkout old-branch
        get pull origin new-branch
        
- Merge from local branch :

        git checkout dev
        git merge my-work

7. Recover lost commits within a day

- Use `git reflog` to check on what happen

- Then use `git reset --hard <change>` again to reverse.

        git reset --hard HEAD^
        HEAD is now at 1a75c1d... added file1

        $ cat file2
        cat: file2: No such file or directory

        $ git reflog
        1a75c1d... HEAD@{0}: reset --hard HEAD^: updating HEAD
        f6e5064... HEAD@{1}: commit: added file2

        $ git reset --hard f6e5064
        HEAD is now at f6e5064... added file2
        
8. Pull a certain branch from remote 

        git branch -f remote_branch_name origin/remote_branch_name
        git checkout remote_branch_name
        
9. Save credential 

        git config --global credential.helper osxkeychain
