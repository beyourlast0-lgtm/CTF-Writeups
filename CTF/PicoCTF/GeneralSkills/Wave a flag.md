# PicoCTF - Wave a flag

## 📌 Problem
- Category: General Skills
- Difficulty: Easy
- Description: 실행 파일을 통해 flag를 얻는 문제

## 🧠 Approach
- 파일을 열어보니 사람이 읽을 수 없는 ELF 바이너리 형태였다.
- 텍스트 파일이 아니라 실행 파일임을 확인하고 실행을 시도했다.
- 실행 후 출력된 메시지에서 `-h` 옵션을 사용하라는 힌트를 얻었다.

## 🧪 Solution
Kali Linux 환경에서 파일을 실행했다.

```bash
chmod +x warm
./warm
출력된 안내 메시지에 따라 help 옵션을 사용했다.

./warm -h
해당 옵션을 사용하자 flag가 출력되었다.

🚩 Flag
picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
📚 Takeaways
바이너리 파일은 열어보는 것이 아니라 실행해야 한다.

실행 파일에서 -h 또는 --help 옵션은 가장 먼저 확인할 가치가 있다.

리눅스 환경(Kali)을 사용하면 CTF 문제 풀이가 훨씬 수월하다.

🔁 One-line Summary
실행 파일의 도움말 옵션을 활용해 flag를 획득하는 문제였다.


---

```bash
git add .
git commit -m "picoCTF: General Skills - Wave a flag"
git push
