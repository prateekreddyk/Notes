### John's workflow session notes

What is a workflow?

Any activity in our daily life where we have to make series of decisions to execute something templatized, to a structure that we can execute it like an algorithm to improve our effiency and accuracy while avoiding mental fatigue.

##### Acronynm SAPS:
* Squence
* Actions
* Purpose
* Signal

`SQUENCE of ACTIONS for a specific PURPOSE executed on a SIGNAL/trigger`

------
An example of what can be a workflow that we can relate in our day to day life

```mermaid
flowchart TD;
    subgraph workflow[John's recurring cost flow]
        A[Annualize the cost] ==> B[Check for an alternative]
        B -.Found a better alternative.->A
        B ==> C{Gut check}
        C -->|Good| D[Go for it]
        C -->|Nuetral/No| E[Skip it]
        C -->|worse| F[Stay away]
    end
```

------
The workflow I can relate to was a trading strategy where you have to meticulously follow same series of steps for everyday for success and any deviations could lead to more probabilty of losses. 

```mermaid
graph TD;
    subgraph tradeplan[Generic trade plan flow]
        a[identify a stock] ==> b[go thru the checklist like volatility,volume etc..,]
        b -.doesn't satisfy checklist.-> a
        b ==> c[assess the risk reward]
        c ==> f{take the trade}
        f -->|Yes| d[ if reward criteria is met]
        f -->|No| e[if doesn't]
    end
```

-----
At work this can applied to lot of stuff. Like CI/CD pipelines, AWS Step Functions, Decisions rules which are similar to the workflow. And the event drive design perfectly fits into this. 

```mermaid
flowchart LR;
    subgraph pipeline[Sample CI pipeline flow example]
    direction LR
        A[Commit to the repo] --> B[Kicks of the pipeline]
        B --> C[Scans thru the source code for complicance checks & secrets]
        C --> D[validates all the inputs]
        D --> E[Executes the build]
        E --> F[Runs test cases]
        F --> G[Scan SAST,DAST,SONAR,SCA]
        G --> H[Publish artifact to repository/artifactory]
        H --> I[Update BOM]
    end
```

------

While I still can't completely comprehend on how to put this to use in my daily routine, this definitely helps me in streamlining my work proccesses where I have a hybrid approach using pipelines/automation and some manual effort for completing a task. This helps make sure that I wouldn't miss a step. Also can help with troubleshooting flow where multiple systems are interracted in a series/routine. 
