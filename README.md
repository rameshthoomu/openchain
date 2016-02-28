##Continuous Integration Process:#


Continuous Integration is a development practice that require developers to integrate code into a shared repository. Each time developer checks in the code into the repository is then verified by an automation build process. This process gives felixibilty for the developer to detects the build issues early.


**OpenBlockChain** Project is having an automation build process and it gives the developer and the contributors to see results of their build results early.


We have used **Travis CI** tool as a Continuous Integration tool and maintaining obc-peer repository in **GIT HUB**.


**Master Repository** can be found in [OpenBlockChain](https://github.com/openblockchain/obc-peer.git)


##Setting up Continuous Integration Process:


- Fork the [**OpenBlockChain**](https://github.com/openblockchain/obc-peer.git) project into your *GITHUB* account. please ignore this step if you have already forked the *OpenBlockChain* project into your working GITHUB repository.


#####Enabling the **Travis CI** integration in **GIT HUB**:


- Click on **Settings** tab in the forked the obc-peer repository and click on **Webhooks & Services**. On the Right side planel of the window, click on the **Browse the directory** below the services option and enable the **Travis** service.

Once the Travis CI service is enabled you can see the Travis CI service below the Services option.


**Enable and Sync the obc-peer repository in Travis**


- Login into [Travis CI](http://travis-ci.org) and click on **Sign in with GitHub** button Travis CI prompt you to enter the GitHub Login credentials and click on Sign in Button.


- Once login into the Travis CI - Click on the *Accounts* link and click on the **Sync account** button. You will see the obc-peer repository below and flick the repository button. If the sync is successfull you can see the synced repository in *My Repository* on the right hand click on **Settings** below the **More Options** button and enable all four options like **Build only if .travis.yml is present**   **Build Pushes**   **Limit Current jobs**   **Build pull requests**

                   Now you are completed with the Travis CI integration with the GitHub.

**Enable the .travis.yml file** as per user needs:
Install:
```
git clone https://github.com/rameshthoomu/obc-peer.git
```

**to**

```
git clone https://github.com/<GitHub_UserName>/obc-peer.git
```
Change the notifications settings:
```
notifications:

slack:
 on_success: always
 on_failure: always

  email: true
  email:
    recipients:
      - one@example.com
      - other@example.com
    on_success: [always|never|change] # default: change
    on_failure: [always|never|change] # default: always
  ```
