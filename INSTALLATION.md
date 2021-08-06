## Conda env setup
- conda create --name hsn36 python=3.6- 
  - 주의 사항. python 3.5를 권장하는데 3.6을 설치해서 잘 된다고 해서 3.6으로 함. 3.5는 현재 update 안되고 있음
  - 아래와 같이 python 환경 만들고 복사해서 써도 됨
    - conda create --name py36 python=3.6
    - conda create --clone py36 --name hsn36
- conda activate hsn36- 
- pip install -r requirements.txt
  - 주의 사항. 선행 설치되어 있어야 하는 apt
    - sudo apt-get install g++ (확실)
    - pip install cython (불확실)
    - pip install pandas
  - GPU 버전의 경우 toolkit 설치
  - conda install cudatoolkit=10.0
  - conda install cudnn=7.6.5

## Git setup
- git clone https://github.com/jongtaeklee/hsn_v1.git
- git remote add origin https://github.com/jongtaeklee/hsn_v1
- git commit -a -m "Change titles and styling on homepage"
  - 고친거 전체 commit. 앞에 커밋 지우고 이걸로 대체하려면 --amend 추가
- git push -u origin master
  - 아이디 비번: jongtaeklee@gmail.com / 1!

## jupyter setup
- conda install ipykernel
- python -m ipykernel install --user --name hsn36 --display-name "hsn36"
- jupyter notebook --generate-config
- nano ~~/jupyter/jupyter_notebook_config.py
  - c.NotebookApp.allow_origin = '*' #allow all origins
  - c.NotebookApp.ip = '0.0.0.0' # listen on all IPs
- jupyter notebook password

## SVS File I/O
- pip install openslide-python
  - install openslide python
  - 