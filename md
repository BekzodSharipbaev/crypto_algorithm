import hashlib
def get_md5_hash(data):
  """
  Вычисляет MD5-хеш для заданных данных.
  Args:
    data: Данные, для которых нужно вычислить хеш (строка или байты).
  Returns:
    MD5-хеш в виде шестнадцатеричной строки.
  """
  # Преобразуем данные к байтам, если необходимо
  if isinstance(data, str):
    data = data.encode('utf-8')
  # Создаем объект MD5
  md5_hasher = hashlib.md5()
  # Обновляем объект хеширования данными
  md5_hasher.update(data)
  # Вычисляем хеш
  digest = md5_hasher.digest()
  # Возвращаем хеш в виде шестнадцатеричной строки
  return digest.hex()
# Пример использования
data = "Bekzod"
md5_hash = get_md5_hash(data)
print(md5_hash)  # Выведет: 3a4025eb47e2d53f8610d69e95c8d78c

