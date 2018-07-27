CCFLAGS=-I/home/zilong/WorkSpace/disk0/ffmpeg/libs/include -O2   
LDFLAGS=-L/home/zilong/WorkSpace/disk0/ffmpeg/libs/lib -Wl,--start-group -lavformat -lavfilter -lavcodec -lswresample -lavdevice -lavutil -lswscale -lpostproc -lpthread -lm -lx264 -lz -lSDL2 -lbz2 \
	-lX11 -Wl,--end-group 
TARGET=myplayer  
OBJS=app.o  
RM=rm -f  
STRIP=strip  
  
$(TARGET):$(OBJS)  
	$(CC) -o $(TARGET) $(OBJS) $(LDFLAGS)  
#	$(STRIP) $(TARGET)  
  
$(OBJS):%.o:%.c  
	$(CC) -c $(CCFLAGS) $< -o $@  
  
clean:  
	$(RM) $(TARGET) $(OBJS) *~ 
