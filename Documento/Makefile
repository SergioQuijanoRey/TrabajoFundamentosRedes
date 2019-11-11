# Makefile para generar el documento de latex en un formato adecuado

help:
	@echo "Makefile para generacion del documento"
	@echo "	make pdf: genera el pdf del trabajo"
	@echo "	make clean: limpia los archivos auxiliares generados en la compilacion"
	@echo "	make deepclean: limpia todos los archivos salvo el latex y adjuntos"

pdf:
	@pdflatex Trabajo.tex

clean:
	@rm -f *.log
	@rm -f *.aux
	@rm -f *.toc

deepclean:
	@make clean
	@rm *.pdf
