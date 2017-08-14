## Как ведет себя Сафари в приватном режиме с localStorage

1. `localStorage.getItem()` возвращает `null`;
2. `localStorage.setItem()` выкидывает исключение `QuotaExceededError (DOM Exception 22): The quota has been exceeded`.
