# ansible-playbook
ansible-playbook - shellscript.yml
- 스크립트는 별도로 작성해야함. file name : startrun.sh
- startrun.sh 파일을 files/startrun.sh 에 위치 시키기 
- 해당 스크립트는 별도의 ">",  ">>" 등으로 파일 리다이렉션을 하면 안 되고 console 에 뿌려져야 ansible 이 수집함.
ex)
#!/bin/sh
ip -o -4 a

- 실행되어 수집된 파일은 localhost 의 /tmp/gahter-all/* 에 hostname_result.txt 형태로 수집됨.
