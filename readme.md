Для порівняння ефективності методів сортування зробимо три вибірки даних:
на 1 000, 10 000 і на 50 000.
Ці дані обираються серед цілих чисел у відповідних межах (1000, 10000 і 50000) за допомогою функції random.
Результати такого тестування наведені у наступній таблиці:

| Algorithm          | Time small data      | Time medium data     | Time big data       
|------------------- | -------------------- | -------------------- | --------------------
| Insertion sort     | 0.50056              | 44.45434             | 1214.14592
| Merge sort         | 0.04187              | 0.42345              | 2.39997
| Timsort sorted     | 0.00117              | 0.01865              | 0.11233
| Timsort sort       | 0.00111              | 0.01857              | 0.10793

Тож, як бачимо, серед обраних методів, метод вставки найповільніший. При чому, чим більше даних, тим повільніше він відпрацьовує.
Метод злиттям вже набагато швидший, і, чим більший об'єм даних для сортування, тим більше помітна різниця у швидкості між цими двома методами.
Для перевірки Timsort алгоритму візьмемо обидві функції: sorted і sort
Як бачимо з таблиці, обидва варіанти sorted і sort працюють значно швидше, ніж алгоритм сортування злиттям і вставкою. 
Як бачимо, між самими цими функціями sorted і sort теж є різниця. І ця різниця зберігається як на невеликих даних, так і на даних в 50 000.
Тож функція "sort" виявилася найшвидшою, що тим більше помітно, чим більші дані для сортування на вході.
У будь якому випадку, обидві функції sorted і sort працюють в багато разів швидше, ніж алгоритм сортування злиттям, і, тим паче, ніж алгоритм сортування вставками.
Таким чином для великих даних використання вбудованих фукнцій Timsort має беззаперечну перевагу. Що дуже економить час виконання таких дій у додатках.
Тож, у цьому дослідженні ми переконалися емпіричнім методом, що, у більшості випадків, набагато ефективніше використовувати вбудовані в Python функції сортування, ніж кодувати їх самостійно.
