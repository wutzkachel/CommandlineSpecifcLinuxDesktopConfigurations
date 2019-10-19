# Installation 
 
## pipenv 
 
 * **Install pip** 
    ```
    curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
    ``` 
    ```
    python2 get-pip.py --user
    ``` 
 * **Upgrade pip** 
    ```
    pip install --upgrade pip --user
    ``` 
 * **Install pipenv** 
    ```
    pip install --user pipenv
    ``` 
 * **Insert PATH Variable in .bash_profile** 
    ```
    export PATH=$PATH:/home/michael/.local/bin
    ``` 
## ansible 
 
 * **Create directory for pipeenv ansible project** 
    ```
    mkdir pipenv && cd pipenv && pipenv --python 3.7
    ``` 
 * **Edit Pipe and  write the ansible version in packages section** 
``` 
[packages] 
ansible = "~=2.8" 
ansible-vault = "*" 
boto = "*" 
botocore = "*" 
boto3 = "*" 
awscli = "*" 
 
[requires] 
python_version = "2.7" 
``` 
  * **Activate ansible virtualenv** 
    ```
    pipenv shell
    ``` 
  * **Remove pip install script** 
    ```
    rm get-pip.py
    ``` 
  * **Create encrypted credentials file** 
    ```
    ansible-vault create credentials.yml
    ``` 
## AWS Cli 
 
  * **Install the AWS Cli with pip** 
    ```
    pip install awscli --upgrade --user
    ``` 
## Git 
 
  * **Store the user credentials** 
 
    ```git config credential.helper store``` 
 
## Zsh     
  * **Installation**
  
  https://github.com/robbyrussell/oh-my-zsh
  
  https://github.com/caiogondim/bullet-train.zsh
    ```
    sudo pacman -S powerline-fonts
    ```
    ```
    yay --answerclean y --answerdiff n --answeredit n ttf-ancient-fonts
    ``` 
