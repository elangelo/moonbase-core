(

  make                                                          &&
  prepare_install                                               &&
  cp iwconfig iwgetid iwlist iwspy iwpriv /sbin/                &&
  cp iwconfig.8 iwlist.8 iwspy.8 iwpriv.8 /usr/share/man/man8/  &&
  cp libiw.so.${VERSION} /lib/                                  &&
  install -m644 iwlib.h /usr/include/                           &&
  install -m644 wireless.h /usr/include/                        &&
  ln -sf /lib/libiw.so.${VERSION} /lib/libiw.so                 &&
  ldconfig                                                      &&

  # Prevent gather_docs from wrongly identifying C files as docs
  rm -f sample_*.c                                              &&
  gather_docs HOTPLUG.txt PCMCIA.txt

) > $C_FIFO 2>&1
