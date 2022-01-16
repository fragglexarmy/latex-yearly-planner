# latex-yearly-planner

PDF planner designed for e-ink devices.

Based on the amazing work of Vitaliy Kudryk (kudrykv) 
See [discussions](https://github.com/kudrykv/latex-yearly-planner/discussions) for available planners and their variations.
Please go investigate this work from Vitaliy if you want to use this. I am simply working on this for my own purposes and to create a custom bullet journal that works for me.

# Build process (From memory so this is just for me to redo if any issues)

1. Install Rocky Linux virtual machine deciated to purpose of building journals for my supernote
2. Upgrade Rocky Linux
3. Install LaTex from the official site as the built in Rocky Linus insatllations is incomplete - http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz
4. Execute installation execute gunzip on the archive
5. Execute tar -xf on the resulting file
6. cd to the directory and execute the installer - Note this takes over an hour - sudo perl install-tl
7. update catalog again - sudo dnf update
8. sudo dnf install wget
9. wget https://dl.google.com/go/go1.<version numbr>.linux-amd64.tar.gz
10. tar-zxvf install file -C /usr/local
11. Change the path - I completed the following change to the ~/.bash_profile file using nano - 
   export PATH=/usr/local/texlive/2021/bin/x86_64-linux:$PATH:/usr/local/go/bin
12. Load the new path - source ~/bash_profile
13. Forked original github repository by Vitaliy and created a Testing branch
14. Grabbed the original repository using go - go get github.com/fragglexarmy/latex-yearly-planner@testing 
15. Resolve dependencies and download them to teh ~/go/pkg/mod/ location - I have forgotten, think it was a go build in the downloaded folder where the go.mod file is 
16. I then deleted the directory for the branch using sudo rm -r ~/go/pkg/mod/github.com/Latex..... folder which is the root of the branch obtained using go get
17. now in the github.com parent I then used git clone to ensure git functionality using - 
    git clone --branch Testing git@github.com:fragglexarmy/latex-yearly-planner.git  ~/go/pkg/mod/github.com/fragglexarmy/latex-yearly-planner
18. now git status, commit, push, resolve are all available to use
19. began understanding and testing code 

# Preview examples
<img src="https://github.com/fragglexarmy/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/01_annual.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/02_quarter.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/03_month.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/04_week.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/05_day.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/06_day_notes.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/07_day_reflect.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/08_todos_index.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/09_todos_page.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/10_notes_index.png" width="419"><img src="https://github.com/kudrykv/latex-yearly-planner/blob/main/examples/pictures/sn_a5x.planner/11_notes_page.png" width="419">
