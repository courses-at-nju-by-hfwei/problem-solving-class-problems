# Extract problems from pdf

# Usage: make DIR=1-4-algorithm
#        make DIR=1-5-data-structure
#        make

DIR ?= [0-9]*
SRC ?= $(DIR)/*.pdf
TXT = $(SRC:.pdf=.txt)

all:
	@for i in $(SRC); do pdftotext $$i; done
	@for i in $(TXT); do echo $$(dirname $$i); grep 题目 $$i | nl -n ln | sed -e '/.*题目 [0-9]\+ ([0-9]\+-[0-9]\+-[0-9]\+)/d' -e 's/\([0-9]\+\).*题目 \([0-9]\+\) /\1 \2：/g' -e 's/\([0-9]\+\).*题目 /第\1题：/g' -e 's/：(/：/g' -e 's/)$$//g' -e 's/^\([0-9]\+\) \1/第\1题/g' -e 's/^[0-9]\+ \([0-9]\+\)/选做\1/g'; echo; done
	@rm -f $(TXT)
