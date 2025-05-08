# Single-linked-list

Реализации собственного односвязного списка.

## Структура проекта

```mermaid
    classDiagram
    class SingleLinkedList~Type~ {
        - Node head_
        - size_t size_
        - void Assign~ItType~(const ItType& first, const ItType& last)

        + SingleLinkedList()
        + SingleLinkedList(std::initializer_list<Type> values)
        + SingleLinkedList(const SingleLinkedList& other) 
        + void swap(SingleLinkedList& other)
        + ~SingleLinkedList()
        + BasicIterator~Type~begin()
        + BasicIterator~Type~end()
        ...()
    }
    class BasicIterator~ValueType~ {
        - Node* node_
        - BasicIterator(Node* node)
        
        + BasicIterator()
        + BasicIterator(const BasicIterator~Type~& other)
        + bool operator==(const BasicIterator~const Type~& rhs)
        + bool operator!=(const BasicIterator<const Type>& rhs)
        + BasicIterator& operator++()
        + BasicIterator operator++(int)
        + ValueType& operator*()
        + ValueType* operator->() 
    }
    SingleLinkedList *-- BasicIterator
```
<br>

### Основные структурные элементы

Основным элементов является шаблон класса односвязного списка. В нем реализованы методы для работы со списком, а так же содержится определение шаблона класса соответствующего итератора.

### Используемые иснтрументы

- компилятор: gcc 11.4.0
- стандарт языка: С++17
- отладчик: GNU gdb 12.1

## Download

Скачать репозиторий можно с помощью команды:

```
git clone git@github.com:alexkozlovvv/cpp-single-linked-list.git
```

## Usage

На данном этапе проект не предполагает интерактивного взаимодействия с пользователем поскольку отсутствует обработка входных команд. При запуске встроенный тест создает односвязный список, проверяет правильность работы методов и взаимодействия со списком с помощью итераторов. 


