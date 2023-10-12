# TCL_LE_AUDIO_LOG

LE audio的排帧是lld_ci_sched或者lld_bi_sched，10ms或者7.5ms一个包, 40个字节(16K)或者155个字节(48K)

在EM fifo  RX中断来了之际，还没到END中断的时候，就将这个40字节或者155字节进行解码，编码TX类似，在下一帧RX或者TX fifo中断到来之前，必须解码完成
