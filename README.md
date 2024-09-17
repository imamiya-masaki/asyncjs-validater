[pages](https://imamiya-masaki.github.io/asyncjs-validater/)
# 概要

scheduler API とか async とか microtask idlecallbackとかややこしいから調べる
基本GPT産

sleeponly 

simple-async => そのまま実行されてしまう (CPUを独占)
simple-async-withtimeout => (suffix -sleepとは若干違うので留意)timeout順に実行されるが、useractionなどは差し込まれる

scheduler (default) => usertaskが割り込みされる
scheduler (background) => usertask,別のタスク両方が差し込まれる
scheduler (yield) => usettaskが割り込まれる

queuemicrotask => そのまま実行されてしまう
queuemicrotask-sleep => そのまま実行されてしまう (マイクロタスクの方が優先度が高いため、settimeoutに行かないのだ)

requestidlecallback => 最初の一度目は、idle状態なので実行されるが、それ以外では、タスクの優先度を遅くする

[/queuemicrotask-sleep.html](/queuemicrotask-sleep.html)

[/queuemicrotask.html](/queuemicrotask.html)

[/requestidlecallback.html](/requestidlecallback.html)

[/scheduler-background](/scheduler-background.html)

[/scheduler-yield](/scheduler-yield.html)

[/scheduler](/scheduler.html)

[/simple-async-withtimeout](/simple-async-withtimeout.html)

[simple-async](/simple-async.html)

[sleeponly](/sleeponly.html)