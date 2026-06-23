# Llama-Local-Chat
Local Llama Chat, full free search, scraping, memory and many more

<img width="1354" height="838" alt="2" src="https://github.com/user-attachments/assets/991ac338-1c5e-46d2-baaa-f6bd4e29ecdd" />
<img width="1907" height="836" alt="1" src="https://github.com/user-attachments/assets/85847bf1-46ce-4274-b259-47c0f42273fe" />


English:

Local LLM Chat — Your Local AI Assistant Powered by llama.cpp (english\russian)
Local LLM Chat is a desktop GUI application for chatting with large language models via llama.cpp (llama-server).
It runs fully locally, requires no internet (except optional search), and provides built‑in tools: web search, page scraping, file/PDF reading, long‑term memory, and more.

End‑user friendly — download or clone the script, install dependencies, and run it with a GUI.

No CLI required — everything is managed through the interface (server start/stop, model selection, parameter tuning).

Full data control — all requests, files, and chat history stay on your computer.

✨ Features
💬 Smart Chat
Supports any GGUF model compatible with llama.cpp (Llama 3, Mistral, Qwen, DeepSeek, etc.)

Markdown rendering (code, lists, quotes, links) with syntax highlighting

Collapsible “Thought” blocks for models that output <think> tags

Dark/light theme, switch on the fly

🛠 Built‑in Tools (Function Calling via text patterns)
🌐 Web Search via SearXNG (local metasearch) — finds news, articles, documents

📄 Web Scraping (scrape_url, extract_links, search_page) — extracts text, links, metadata

📁 File Handling – read_file (text files), read_pdf (via pypdf)

🧠 Long‑Term Memory (memory_write/read/delete) — model remembers preferences, facts, corrections

🔌 Seamless llama.cpp Integration
Built‑in llama‑server control: start/stop from the UI, set port, threads, GPU layers, context size

Auto‑detection of models in a folder (GGUF)

Support for MTP (Multi‑Token Prediction) – enable speculative decoding with --spec-type draft-mtp

Support for Jinja chat templates – required for reasoning models (Qwen3, DeepSeek‑R1, etc.)

⚡ Performance & Convenience
Streaming responses — text appears gradually, no UI jitter

Stats — time‑to‑first‑token (TTFT), generation speed, token count

History autosave — all dialogs are saved and restored on startup

Edit messages — fix your query or regenerate assistant replies

Export chat to .txt for archiving

🚀 Quick Start
Install llama.cpp – download or build llama-server from llama.cpp.
Place the executable somewhere (e.g., ~/VM/Llama_Prism/bin/llama-server).

Download a GGUF model – get a model file (e.g., from Hugging Face) and place it in a folder of your choice.

Install Python dependencies (Python 3.10+):

bash
pip install pypdf beautifulsoup4 pygments requests pyqt6
Run the script:

bash
python LLM-Chat-Llama-1bit.py
Configure in the GUI:

Set path to llama-server and the folder containing your GGUF models.

Select a model from the dropdown.

(Optional) Start the server by clicking the Start server button.

Adjust parameters (temperature, context limit, system prompt, etc.) in the sidebar.

Chat! – type a message, attach files (📎), and hit Send.

Optional: Set up a local SearXNG instance (default: http://localhost:8080/search) for web search.

🛠️ Example Usage
“Find latest space news and save my preference to memory.”
→ Model calls search, returns headlines, then writes to memory.

“Read config.yaml and tell me its settings.”
→ Calls read_file and processes the content.

“Summarise the article at https://example.com/article.”
→ Calls scrape_url, extracts text, and summarises.

⚙️ Technical Details
Language: Python 3.10+

GUI: PyQt6

HTTP client: requests, BeautifulSoup4

Code highlighting: Pygments (optional)

PDF support: pypdf (optional)

Persistence: SQLite (memory), JSON (chat history)

Backend: llama.cpp’s llama-server (OpenAI‑compatible API)

The app automatically checks model capabilities (via /api/show if available) and falls back to text‑based tool parsing for models without native function calling.

📦 License
MIT — free to use, modify, and distribute.

🙏 Credits
llama.cpp for the efficient LLM runtime

SearXNG for private metasearch

PyQt for the GUI framework

⭐ Star the project on GitHub if you find it useful!
Issues and suggestions welcome in Issues.

Русский:

Local LLM Chat — ваш локальный AI‑ассистент на базе llama.cpp
Local LLM Chat — это десктопное приложение с графическим интерфейсом для общения с языковыми моделями через llama.cpp (llama-server).
Работает полностью локально, не требует интернета (кроме опционального поиска) и предлагает встроенные инструменты: веб‑поиск, скрапинг страниц, работа с файлами/PDF, долговременная память и другое.

Для конечного пользователя — скачайте скрипт, установите зависимости и запускайте с графическим интерфейсом.

Без консоли — всё управление через интерфейс (запуск/остановка сервера, выбор модели, настройка параметров).

Полный контроль над данными — все запросы, файлы и история чатов остаются на вашем компьютере.

✨ Возможности
💬 Умный чат
Поддержка любых GGUF‑моделей, совместимых с llama.cpp (Llama 3, Mistral, Qwen, DeepSeek и др.)

Markdown‑разметка с подсветкой синтаксиса

Сворачиваемые блоки «Мысли» для моделей с <think>

Тёмная/светлая тема, переключение на лету

🛠 Встроенные инструменты (через текстовые вызовы)
🌐 Поиск в интернете через SearXNG (локальный метапоиск)

📄 Чтение веб‑страниц (scrape_url, extract_links, search_page)

📁 Работа с файлами – read_file (текстовые), read_pdf (через pypdf)

🧠 Долговременная память (memory_write/read/delete) — модель запоминает предпочтения, факты, исправления

🔌 Интеграция с llama.cpp
Управление llama‑server из интерфейса: запуск/остановка, настройка порта, потоков, слоёв GPU, размера контекста

Автосканирование папки с GGUF‑моделями

Поддержка MTP (Multi‑Token Prediction) – включение спекулятивного декодирования через --spec-type draft-mtp

Поддержка Jinja‑шаблонов чата – необходимо для моделей с рассуждениями (Qwen3, DeepSeek‑R1 и др.)

⚡ Производительность и удобство
Стриминг ответов — текст появляется постепенно

Статистика — TTFT, скорость, количество токенов

Автосохранение истории — диалоги восстанавливаются при запуске

Редактирование сообщений и регенерация ответа

Экспорт чата в .txt

🚀 Быстрый старт
Установите llama.cpp – скачайте или соберите llama-server из репозитория.
Поместите исполняемый файл в удобное место (например, ~/VM/Llama_Prism/bin/llama-server).

Скачайте GGUF‑модель – возьмите модель (например, с Hugging Face) и положите в папку по вашему выбору.

Установите зависимости Python (Python 3.10+):

bash
pip install pypdf beautifulsoup4 pygments requests pyqt6
Запустите скрипт:

bash
python LLM-Chat-Llama-1bit.py
Настройте в интерфейсе:

Укажите путь к llama-server и папке с GGUF‑моделями.

Выберите модель из выпадающего списка.

(Опционально) Запустите сервер кнопкой Запустить сервер.

Отрегулируйте параметры (температура, лимит сообщений, системный промпт и т.д.) в боковой панели.

Общайтесь! – введите сообщение, прикрепите файлы (📎) и нажмите «Отправить».

Опционально: Запустите локальный SearXNG (по умолчанию http://localhost:8080/search) для веб‑поиска.

🛠️ Примеры использования
«Найди последние новости о космосе и сохрани моё предпочтение в память.»
→ Модель выполняет поиск, возвращает заголовки, затем вызывает memory_write.

«Прочитай config.yaml и расскажи, какие там настройки.»
→ Вызывается read_file, содержимое отправляется модели.

«Что написано в статье по ссылке https://example.com/article? Выдели основные тезисы.»
→ Модель вызывает scrape_url, извлекает текст и обрабатывает его.

⚙️ Технические детали
Язык: Python 3.10+

GUI: PyQt6

HTTP‑клиент: requests, BeautifulSoup4

Подсветка кода: Pygments (опционально)

PDF: pypdf (опционально)

Хранение: SQLite (память), JSON (история чатов)

Бэкенд: llama-server от llama.cpp (API, совместимый с OpenAI)

Приложение автоматически определяет возможности модели (через /api/show при наличии) и переключается на текстовый парсинг инструментов для моделей без нативной поддержки.

📦 Лицензия
MIT — разрешено использовать, модифицировать и распространять без ограничений.

🙏 Благодарности
llama.cpp за эффективный движок LLM

SearXNG за приватный метапоиск

PyQt за отличный GUI‑инструментарий

⭐ Поставьте звёздочку на GitHub, если проект полезен!
Сообщения об ошибках и предложения приветствуются в Issues.
