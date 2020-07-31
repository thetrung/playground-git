## QUICK NOTE


1. Reset all un-pushed commits 

        git reset --hard @{u}
      
2. See all git commit in short form

        git log --oneline
      
      
3. Merge N-commits into one or re-arrange them :

        git rebase -i HEAD~N
        
4. Force delete pushed commits :

        git push -u -f origin <commit>:dev

5. Resolve file mode changes, when you see :

        old mode 100755  
        new mode 100644  

- Use this :

        git config core.filemode false
