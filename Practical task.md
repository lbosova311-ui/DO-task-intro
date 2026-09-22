## Practical Task 1 — Working in the Linux command line

Виконано в терміналі Kali Linux (bash).

```bash
mkdir lisa                                          # створюю папку зі своїм ім'ям
cd lisa                                             # переходжу у цю папку
PS1="Bosova> "                                      # змінюю запрошення терміналу на просте "Bosova>"
PS1="\e[0;32m[\u@\h \W]\$ \e[0m"                    # роблю запрошення зеленим, показую користувача, хост і поточну папку
echo '#!/bin/bash' > lisa.sh                        # створюю файл-скрипт, вказую, що це bash-скрипт
echo 'echo "Hi! I am Bosova"' >> lisa.sh             # додаю рядок з привітанням
echo 'echo "$HOME"' >> lisa.sh                       # додаю рядок, що виводить домашню директорію
echo 'echo "$$"' >> lisa.sh                          # додаю рядок, що виводить PID процесу
chmod 776 lisa.sh                                   # надаю файлу права на виконання
./lisa.sh                                           # запускаю скрипт
```

**Результат виконання:**

<img width="572" height="480" alt="image" src="https://github.com/user-attachments/assets/0cac5652-1356-44ab-825f-baa6953ade8a" />

---

## Practical Task 2 — Fork repository + GitHub Pages

**1. Форкнула репозиторій** `mentorchita/my_yourname_site` під власним ім'ям `my_lisa_site`.

<img width="512" height="101" alt="image" src="https://github.com/user-attachments/assets/aa4a87a6-b142-4683-b12e-90eb42ec24bb" />

**2. Увімкнула GitHub Pages** у Settings → Pages: обрала гілку `main`, папку `/(root)`, натиснула Save.

<img width="307" height="122" alt="image" src="https://github.com/user-attachments/assets/10da9ebb-feb4-4ce3-9a51-3ad91cb07f0f" />

**3. Додала Repository Secret** у Settings → Secrets and variables → Actions: `MY_SECRET_NAME` = `Lisa Bosova`.

<img width="1023" height="757" alt="image" src="https://github.com/user-attachments/assets/6bdcdecc-4bd8-42f9-be8d-fab4dd3e0f76" />

**4. Запустила workflow** "Deploy static content to Pages" вручну (Run workflow) на вкладці Actions.

<img width="396" height="113" alt="image" src="https://github.com/user-attachments/assets/5db0febe-50ca-4c78-bde3-ce190fb0663e" />

**5. Результат — опублікований сайт** з моїм ім'ям на GitHub Pages.

<img width="1462" height="868" alt="image" src="https://github.com/user-attachments/assets/175c85cf-5669-4645-b0fc-51288ce4612c" />
