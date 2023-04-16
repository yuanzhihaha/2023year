#	$(foreach var, list, text)	#从列表list中每取出一个var,执行一次text的语句
A = a b c
B = $(foreach f, $(A), $(f).o)	
C = $(foreach f, $(A), zyz)		

D = a b c d/
#	$(filter pattern..., text)	# 在text中取出符合patten格式的值
E = $(filter %/, $(D))			
#	$(filter-out pattern..., text)	# 在text中取出不符合patten格式的值
F = $(filter-out %/, $(D))		

# 	$(wildcard pattern)		# pattern定义了文件名的格式，wildcard取出其中存在的文件
files = $(wildcard *.c)		#找出所有的.c文件

files2 = a.c b.c c.c d.c e.c abc	
files3 = $(wildcard $(files2))	#找出files2中所有存在的文件

#	 $(patsubst pattern, replacement, $(var))	#从var列表中取出每一个值，如果符合pattern，则替换成replacement
_files = $(patsubst %.c, %.c++, $(files2))	#找出.c,替换成.c++
all:
	@echo A = $(A)
	@echo B = $(B)
	@echo C = $(C)
	@echo E = $(E)
	@echo F = $(F)
	@echo files = $(files)
	@echo files3 = $(files3)
	@echo _files = $(_files)