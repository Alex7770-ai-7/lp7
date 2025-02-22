result = []

def divider(a, b):
    try:
        if not isinstance(a, (int, float)) or not isinstance(b, (int, float)):
            raise TypeError("Операнди повинні бути числами")
        if a < b:
            raise ValueError("a повинно бути більше або рівне b")
        if b > 100:
            raise IndexError("b не повинно бути більше 100")
        return a / b
    except Exception as e:
        print(f"Помилка: {e}")
        return None

# Виправлений словник даних ("123" -> число, [] -> видалено, бо ключ повинен бути хешованим)
data = {10: 2, 2: 5, 123: 4, 18: 0, 8: 4}

for key, value in data.items():
    res = divider(key, value)
    if res is not None:
        result.append(res)

print(result)
