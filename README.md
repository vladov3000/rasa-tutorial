# rasa assistant

## Google Cloud VM setup

1. Go to https://console.cloud.google.com/
2. Sign in with .edu
3. Activate Google Cloud $300 credit (requires credit card but no autocharge)
3. Click on the project select button right next to the "Google Cloud Platform" logo in the upper left
4. Select "New Project" in the upper right of the pop up
5. Create a new project called rasa
6. On the sidebar select Compute Engine -> VM Instances
7. Create VM instance:
8. Machine type set to n1-standard-4(4 vCPU, 15 GB memory)
9. Change Boot Disk Image to 100 GB Ubuntu 16.02
10. Create instance
11. Click on ssh button for instance
12. git clone https://github.com/vladov3000/rasa-tutorial.git
12. cd rasa-tutorial
13. sudo apt-get update
14. sudo apt install python3-pip
15. pip3 install -r requirements.txt
16. rasa train
17. rasa run actions (in seperate window)
18. rasa shell

Enviroment setup:

    Ubuntu 19
    python version: 3.7.5
    pip version: 20.1.2
    pip3 install -r requirements.txt
    
Or use virtual env (will be have to be done for every tmux window):

    python3 -m venv ./venv
    source /venv/bin/activate
    pip install -r requirements.txt

To run rasa with command line shell:

    rasa train
    rasa run actions (in seperate window)
    rasa shell
    
To run tests:

    rasa test --stories tests/conversation_tests.md
