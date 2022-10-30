#### CI/CD
automate the stages of app development
CI - continuous integration - automation process

    branch-change -review-merge to main of the pipeline



 ```mermaid
   stateDiagram
   direction LR
    [*] --> main
    main --> branch : 1
    state branch {
    direction LR
    change --> review : 2
    review --> merge : 3
    }
    merge --> main : 4
    main --> ansible : 5 git pull
    state network {
    ansible --> router : 6 playbook
    }
 ```
 
