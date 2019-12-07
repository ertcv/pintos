# pintos

<pre>
1. alarm-single: pass
2. alarm-multiple: pass
3. alarm-simultaneous: pass
4. alarm-priority: pass
5. alarm-zero: pass
6. alarm-negative: pass
7. priority-change: pass
8. priority-change-2: pass
9. priority-fifo: pass
10. priority-lifo: pass // pintos -v -- -q run priority-lifo (can't be checked by make check)
11. priority-preemp: pass
12. priority-sema: pass
13. priority-aging: pass
-----------------------------------
Additional Requirement - BSD Scheduler (5%)
  1. mlfqs-block: FAIL
  2. mlfqs-fair-2: FAIL
  3. mlfqs-fair-20: FAIL
  4. mlfqs-load-1: FAIL
  5. mlfqs-load-60: FAIL
  6. mlfqs-load-avg: FAIL
  7. mlfqs-nice-10: FAIL
  8. mlfqs-nice-2: FAIL
  9. mlfqs-recent-1: FAIL
</pre>

/// 하나만 검사하는 명령어 (pintos/src/userprog/build 에서 수행)
pintos -v -k -T 60 --qemu --filesys-size=2 -p tests/userprog/sc-bad-sp -a sc-bad-sp -- -q -f run sc-bad-sp

// pintos/src/tests/threads/Make.tests 12개만 검사 되도록 수정함 -> 제출 전에 원래 파일로 다시 수정하기
pintos -v -- -q run priority-lifo
