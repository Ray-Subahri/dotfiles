FILE := NAME
OUT := build
NAME := 'NAME'

.PHONY: pdf
pdf:
	latexmk -interaction=nonstopmode -outdir=$(OUT) -pdf -halt-on-error $(FILE).tex;
	mv $(OUT)/$(FILE).pdf $(OUT)/$(NAME).pdf;

.PHONY: watch
watch:
	latexmk -interaction=nonstopmode -outdir=$(OUT) -pdf -pvc -halt-on-error $(FILE).tex;

.PHONY: clean
clean:
	rm -rf $(filter-out $(OUT)/$(FILE).pdf, $(wildcard $(OUT)/*))

.PHONY: purge
purge:
	rm -rf $(OUT)
