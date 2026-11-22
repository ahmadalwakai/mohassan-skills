---
name: البرمجة بلغة Python
description: البرمجة بلغة بايثون: سكربتات، مكتبات، البيئة الافتراضية، pip، الملفات، الاستثناءات، الأداء، الأنواع، الاختبار. python py pip venv virtualenv poetry pandas numpy pathlib script asyncio typing pytest django flask fastapi بايثون بايثن البايثون سكربت سكريبت
version: 1.0.0
category: coding
---
Use this for Python code, scripts, packaging and language questions.
1. Target a current Python 3 release and state the minimum version the code needs. One virtual environment per project (`python -m venv venv`), dependencies pinned in requirements.txt or pyproject.toml with a lock file.
2. Idiomatic code: pathlib for paths, context managers (`with`) for files and locks, f-strings, comprehensions for simple transforms, dataclasses or TypedDict for structured data, type hints on public functions.
3. Open text files with `encoding="utf-8"`, which matters for Arabic text. Use the csv module or pandas for CSV and json for JSON; never parse them with split.
4. Errors: catch specific exceptions, never a bare `except:`; let unexpected ones surface with their traceback; use logging rather than print in anything long-running.
5. Performance: measure first (timeit, cProfile). Prefer built-ins and vectorized pandas or NumPy over Python loops on large data, generators for streams, asyncio or threads for I/O-bound work and multiprocessing for CPU-bound work.
6. Scripts get a `main()` function, `if __name__ == "__main__":`, and argparse for options.
7. Tests with pytest: small functions, fixtures for setup, one behaviour per test.
8. Any script that deletes or overwrites files gets a dry-run option and an explicit path check.
Answer shape: working code with imports, the command to run it, and what output to expect.
