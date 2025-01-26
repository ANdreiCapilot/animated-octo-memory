import hashlib

def brute_force_md5(target_hash):
    for i in range(1000000):  # Пробуем числа от 0 до 999999
        test_string = str(i)
        test_hash = hashlib.md5(test_string.encode()).hexdigest()
        if test_hash == target_hash:
            return test_string
    return None

target_hash = '4f36b818078a75703b8284ac23f48d69'
result = brute_force_md5(target_hash)
print(f'Загаданное число: {result}')
