# (追加) スケジューラが起動するタイミング

* 割り込み処理終了時
* 実行中のプロセスの意思
  * 待機状態に遷移
  * sched_yield()
* プリエンプト(奪う)
  * TASK_RUNNING になった時
  * クォンタム時間を使い切った

# (追加) プロセスディスパッチ契機

* プロセスを生成した時
* プロセスを終了した時
* 実行プロセスが待機状態に遷移した時
* プロセスが待機状態から復帰した時
* 実行プロセスがタイムスライスを使いきった時
* カーネルプリエンプションした時
* システムコールによって明示的にプロセス切り替えを行った時(sched_yield(2))
* システムコールによってスケジューリングポリシーを変更した時
* システムコールによって静的優先度を変更した時

