# Куча ядра
Куча ядра является двусвязным списком используемым для выделения памяти под нужды ядра.


## void kheap_init()
kheap_init - используется для инициализации кучи ядра.


## void *kheap_morecore(uint32_t size)
kheap_morecore - увеличивает кучу ядра на некоторый размер(uint32_t size), он будет округлен до размера страницы.
Возвращает адрес выделеной памяти.


## int kheap_free(void *address)
kheap_free -  освобождения выделенного элемента(void *address) из кучи ядра.
Возвращает 1 в случае успешного выполнения, -1 в случае ошибки.


## void *kheap_malloc(uint32_t size)
kheap_malloc - выделяет произвольного размера памяти(uint32_t size) из кучи ядра.
Возвращает выделенную ячейку памяти(void*).


## void kheap_print_stat()
kheap_print_stat - выводит информацию о состоянии kheap.