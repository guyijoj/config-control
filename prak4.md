# ЗАДАЧА 1
Написать программу на Питоне, которая транслирует граф зависимостей civgraph в makefile в духе примера выше. Для мало знакомых с Питоном используется упрощенный вариант civgraph: civgraph.json.

**ПРИМЕР**  
```
> make mathematics
mining
bronze_working
sailing
astrology
celestial_navigation
pottery
writing
code_of_laws
foreign_trade
currency
irrigation
masonry
early_empire
mysticism
drama_poetry
mathematics
```
**РЕШЕНИЕ**  
```
import json

# Загрузка графа из JSON файла
def load_civgraph(file):
    with open(file, 'r') as f:
        return json.load(f)

# Функция для генерации Makefile
def generate_makefile(civgraph, target):
    visited = set()  # Для отслеживания посещенных задач
    result = []

    # Рекурсивная функция обхода зависимостей
    def visit(tech):
        if tech in visited:
            return
        visited.add(tech)
        for dep in civgraph.get(tech, []):
            visit(dep)
        result.append(tech)

    # Посещаем целевую технологию
    visit(target)

    # Печатаем задачи в порядке их выполнения
    for task in result:
        print(task)

if __name__ == '__main__':
    civgraph = load_civgraph('civgraph.json')
    target = input('Enter the target technology: ')  # Например, mathematics
    generate_makefile(civgraph, target)
```
