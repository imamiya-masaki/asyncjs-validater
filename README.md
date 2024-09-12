# 概要
scheduler API とか async とか microtask idlecallbackとかややこしいから調べる
基本GPT産

simple-async => そのまま実行されてしまう (CPUを独占)
simple-async-withtimeout => timeoutが差し込まれるタイミングで別のタスクにCPUを渡す (その後自分自身を実行する)

scheduler (default) => usertaskが割り込みされる
scheduler (background) => usertask,別のタスク両方が差し込まれる
scheduler (yield) => usettaskが割り込まれる

queuemicrotask => そのまま実行されてしまう (CPUを独占)
queuemicrotask-withtimeout => timeoutが差し込まれるタイミングで別のタスクにCPUを明け渡す(timeoutから復帰するのは、すべてのタスクが終了したとき)

requestidlecallback => 最初の一度目は、idle状態なので実行されるが、それ以外では、タスクの優先度を遅くする

[/queuemicrotask-sleep.html](/queuemicrotask-sleep.html)

[/queuemicrotask.html](/queuemicrotask.html)

[/requestidlecallback.html](/requestidlecallback.html)

[/scheduler-background](/scheduler-background.html)

[/scheduler-yield](/scheduler-yield.html)

[/scheduler](/scheduler.html)

[/simple-async-withtimeout](/simple-async-withtimeout.html)

[simple-async](/simple-async.html)