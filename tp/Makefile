SRC=main
COMMAND= pdflatex -shells-escape $(SRC).tex

all: $(SRC).pdf clean 

.PHONY:quick
quick:
	$(COMMAND)


$(SRC).pdf: $(SRC).tex Makefile
	$(COMMAND)
	$(COMMAND)


.PHONY: view
view: $(SRC).pdf
	nohup evince $(SRC).pdf > /dev/null 2>&1 &

.PHONY: mrproper
mrproper: clean
	rm -rf $(SRC).pdf

.PHONY: clean
clean:
#	rm -f $(SRC).pdf
	rm -f $(SRC).aux
	rm -f $(SRC).log
	rm -f $(SRC).nav
	rm -f $(SRC).out
	rm -f $(SRC).snm
	rm -f $(SRC).toc
	rm -f $(SRC).vrb
	rm -f *.log
