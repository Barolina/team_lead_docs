---
description: коммиты  и  соглашения
---

# git

🔑 x.x.x-dev - имя ветки, в которой ведем совместную разработку. С ней работаем через пулл-реквесты.&#x20;

⚾️ feature/N-tack - личная ветка разработчика, заканчивается на ваш github-username. Ее можно и нужно пушить на GitHub, предлагать сделать код-ревью и т.п.&#x20;

⏰ Регулярно в начале дня выполняйте "git fetch" и, затем, "git merge x.x.x-dev" в свою личную ветку.

&#x20;😴 Регулярно в конце дня отправляйте свои изменения на сервер в своей личной ветке&#x20;

🕹 Ветки для экспериментов, которые вы создаете в локальном репозитории, пушить на GitHub не нужно. Можете называть как угодно. Помните правило - ветвитесь часто. Появилась идея - сделайте ответвление от личной ветки "git checkout -b " и туда уже комиттесь. Если вам понравилось - "git checkout feature/experiment" и "git merge ".&#x20;

🚫 Мы НЕ перезаписываем ветки в удаленном репозитории - DON'T "git push --force origin user\_name/feature/auth"&#x20;

🚫 Мы НЕ выполняем git rebase в своих личных ветках после того - как запушили изменения на удаленный репозиторий (см. The Golden Rule of Rebasing)
