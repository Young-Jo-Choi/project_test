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
    5. package 설치
    ```
    poetry add [package]
    ```
    6. virtual env 
    ```
    poetry shell
    ```
    -----
    ```
    source .venv/bin/activate
    source /home/choiyj/.cache/pypoetry/virtualenvs/project-test-KRnPQjp1-py3.7/bin/activate
    ```
3. Project Structure
    ```
    mkdir -p data/raw data/processed src
    ```

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
    2. git add
    3. git commit

5. Github 연결
    1. git remote add origin https://github.com/Young-Jo-Choi/project_test.git
    2. git branch -M main
    3. git push -u origin main
    4. git push

---
# Only pip
(pyenv local 3.7.13)
1. project 폴더 만들기
2. python -m venv .venv
3. source .venv/bin/activate 
    - vscode에서는 python version(껐다 키면 됨)
4. 사용함.
5. deactivate

# jupyter connection
1. pip install jupyter
2. pip install ipykernel
3. python -m ipykernel install --user --name [.venv] --display-name "[.venv]"

## conda init
1. /home/miniconda3/condabin/conda init
2. source ~/.bashrc
