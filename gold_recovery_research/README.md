# Данные
В таблицах представлены данные по параметрам технологического процесса очистки золота, а также показатель восстановления, получившийся при использовании соответствующих параметров. Данные требуют предобработки.
# Задача
Необходимо построить модель, которая будет предсказывать коэффициент восстановления золота из золотосодержащей руды. Модель поможет оптимизировать производство, чтобы не запускать предприятие с убыточными характеристиками. Метрика качества моделей - sMAPE, причём важно учесть, что необходимо предсказать не только финальный коэффициент, но и коэффициент восстановления после флотации(грубая очистка).
Финальный коэффициент складывается из двух составляющих: `0.25 * sMAPE(rougher) + 0.75 * sMAPE(final)`.

Параметр `recovery` - восстановление расчитывается по формуле: `(C * (F - T)) / (F * (C - T)) * 100%`, где:
* С - доля золота в концентрате после флотации/очистки;
* F - доля золота в сырье/концентрате до флотации/очистки;
* T - доля золота в отвальных хвостах после флотации/очистки.
# Используемые библиотеки
*pandas*, *numpy*, *sklearn*, *matplotlib*, *seaborn*, *LightGBM*