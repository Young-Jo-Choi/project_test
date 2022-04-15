# Start Python Project
## Contents(User)
1. Pyenv - python version 관리 
    1. 설치
        ```
         git clone https://github.com/pyenv/pyenv.git ~/.pyenv
         ```
    2. pyenv path 설정
        ```
        sed -Ei -e '/^([^#]|$)/ {a \
        export PYENV_ROOT="$HOME/.pyenv"
        a \
        export PATH="$PYENV_ROOT/bin:$PATH"
        a \
        ' -e ':a' -e '$!{n;ba};}' ~/.bash_profile
        echo 'eval "$(pyenv init --path)"' >> ~/.bash_profile

        echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.profile
        echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.profile
        echo 'eval "$(pyenv init --path)"' >> ~/.profile

        echo 'eval "$(pyenv init -)"' >> ~/.bashrc
        ```
    3. python 원하는 version 설치
        ```
        pyenv install [VERSION]
        ```
    4. global python  설정
        ```
        pyenv global [VERSION]
        ```
    5. poetry virtual environment 내부에 설치
        ```
        poetry config virtualenvs.create true --local
        ```

2. Poetry - package manager + virtualenv
    1. poetry 설치
    ```
    pip install poetry
    ```
    2. 프로젝트 폴더 만들기
    ```
    mkdir project_test && cd project_test
    ```
    3. python local version 설정
    ```
    pyenv local [VERSIONS]
    ```
    4. 프로젝트 구성
    ```
    poetry init
    ```
3. Project Structure
    ```
        .
    ├── data
    │   ├── processed
    │   └── raw
    ├── document
    ├── explore
    ├── main.py
    ├── poetry.lock
    ├── poetry.toml
    ├── pyproject.toml
    ├── README.md
    └── src
    ```
4. Git init
    1. git init
    ```
    git init
    ```
    2. 
5. Github 연결
