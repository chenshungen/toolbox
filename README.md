# toolbox

exp : find . -iname *.[ch] -exec grep --color -wn -H "$*" {} \;
exp脚本用于从需要检索的文件中检索特定的字符串，默认添加了检索.h .cpp .php文件，如需要检索其他文件类型可自行添加。
用法：exp str
[chen@iZ117mwkj2bZ Libevent]$ exp Event
./http.c:1550: * Event callback for asynchronous connection attempt.
./include/event2/bufferevent_struct.h:71:       /** Event base for which this bufferevent was created. */
./include/event2/event.h:83:  @section event Event notification
./include/event2/event.h:139:  @section evhttp Event-driven HTTP servers
./include/event2/event.h:360:   Event dispatching loop
./evsignal-internal.h:40:       /* Event watching ev_signal_pair[1] */
./event-internal.h:62:/** @name Event closure codes
./event-internal.h:169: /* Event that triggers whenever one of the events in the queue is
./test/regress_bufferevent.c:1060:              TT_BLATHER(("Event successfully triggered."));

类似命令脚本可以使用 find . -name "*" |xargs grep str 此命令没有颜色亮色区分



