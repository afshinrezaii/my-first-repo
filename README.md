
4. `main.py`
```python
#!/usr/bin/env python3
"""
main.py — نمونهٔ ساده CLI که اسم می‌گیرد و پیام می‌زند.
"""
import argparse
from datetime import datetime

def greet(name: str) -> str:
    now = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    
    
    return f"Salam, {name}! (time: {now})"

def main():
    parser = argparse.ArgumentParser(description="Hello GitHub simple CLI
    parser.add_argument("--name", "-n", default="World", help="Name to greet")
    args = parser.parse_args()
    print(greet(args.name))

if __name__ == "__main__":
    main()
