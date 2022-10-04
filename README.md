# ansible-playbook
ansible-playbook - shellscript.yml
특정 스크립트를 수행하고 수행결과를 파일로 저장하여 수집함.

# Note
# 
    스크립트는 별도로 작성해야함. file name : startrun.sh
    startrun.sh 파일을 files/startrun.sh 에 위치 시키기 
    해당 스크립트는 별도의 ">",  ">>" 등으로 파일 리다이렉션을 하면 안 되고 console 에 뿌려져야 ansible 이 수집함.
    ex)
    #!/bin/sh
    ip -o -4 a

실행되어 수집된 파일은 localhost 의 /tmp/gahter-all/* 에 hostname_result.txt 형태로 수집됨.

ansible-playbook - shellscript.yml
yum meta data 를 가지고 rpm 패키지에 대한 의존성 체크를 진행함.

아해 내용 수정 필요. 
# Plase edit the data below
#
    todir: "/tmp/gather-all/"    # 수집될 파일의 경로 
    sdir: "/Admin"               # 대상 서버의 메타 파일을 저장할 최상단 경로 
    sfile: "rhel-7-server-rpms-meta-0929-1443.tgz"   # yum 메타 파일 이름
    pkg_name:                    # 체크할 패키지 이름 명시 
      - kernel
      - nfs-utils

결과는 /tmp/gather-all/(hostname)_yummeta.txt 형태로 저장됨.
