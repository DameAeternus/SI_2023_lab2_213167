# Дамјан Додевски, бр. на индекс 213167 

Control flow graph:
Фотографијата е дадена во кодот.

Цикломатската комплексност на кодот е: 7
Го добив така што E-V+2 (каде Е=33 и V= 28)

Потребно е да имаме вкупно 13 тест случаи за да ги покриеме сите гранки во кодот.
За првиот условен израз if (user==null || user.getPassword()==null || user.getEmail()==null) можеме да направиме два тест случаи, првиот за да биде true, односно да поставиме еден од трите полиња да се празни за да го добиеме RuntimeException, а вториот да не се null ..
За вториот услов if(user.getUsername()==null) за првиот тест случај ќе го поставиме Username-oт на null, за да мора да се изврши user.setUsername(user.getEmail()), а исто така еден тест случај ќе ни е каде getUsername нема да е null. Значи досега имаме 4 тест случаи.
Ни треба уште еден тест случај каде мејлот нема да содржи @ и .
Следните два тест случаи ќе содржат @ и . и ќе влезе во for циклусот каде ќе треба едниот тест случај same да остане на 0, значи allUsers листата да е празна, а другиот same исто да биде 0 ама аllUsers да има веќе постојачки корисници, но меилот и корисничкото име на User-от нема да се совпаѓаат со некои од постоечките корисници.
Потоа ни требаат уште 2 тест случаи во внатрешниот if во for циклусот кој го споредува корисничкото име на постоечкиот корисник со име на корисникот: прво треба името да се совпаѓа со името на постоечкиот корисник, т.е. same+=1; а вториот името да не се совпаѓа.
Потоа ќе ни требаат уште 2 тест случаи за for циклусот кој проверува специјални знаци во лозинката.
Првиот ттест случај ќе треба да содржи специјален знак, а вториот не.
И, на крај ќе ни требаат уште 2 тест случаи каде едниот ќе биде со празно место, а другиот да влезе во последниот for циклус и да заврши со same == 0.

Според Multiple Condition критериумот, за изразот if (user==null || user.getPassword()==null || user.getEmail()==null) имаме вкупно 3 услови кои можат да имаат две можни вредности (true или false). За да ги истестираме сите Conditions, треба да направиме 2^3 односно 8 тест случаи. Првиот ќе биде каде user == null, user.getPassword() == null и user.getEmail() == null.
Вториот тест случај ќе биде кога user е null, user.getPassword() е null и user.getEmail() не е null.
Третиот тест случај ќе биде кога user е null, user.getPassword() не е null и user.getEmail() е null.
Четвртиот тест случај ќе биде кога user е null, user.getPassword() не е null и user.getEmail() не е null.
Петиот тест случај ќе биде кога user не е null, user.getPassword() е null и user.getEmail() е null.
Шестиот тест случај ќе биде кога user не е null, user.getPassword() е null и user.getEmail() не е null.
Седмиот тест случај ќе биде кога user не е null, user.getPassword() не е null и user.getEmail() е null.
И осмиот тест случај ќе биде кога user не е null, user.getPassword() не е null и user.getEmail() не е null, само тогаш нема да се фрли RuntimeException.
