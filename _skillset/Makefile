all: full skills

#all: index.html index.pdf index.docx index.txt

full: index-full.md style.css
	pandoc --standalone --include-in-header=favicon.txt --title-prefix="Complete skillset" -c style.css --from markdown --to html -o ../skillset/index.html index-full.md
	cp style.css ../skillset/style.css

skills: index-skills.md style.css
	mkdir ../skillset/skill
	pandoc --standalone --include-in-header=favicon.txt --title-prefix="Objective skillset" -c ../style.css --from markdown --to html -o ../skillset/skill/index.html index-skills.md

#index.pdf: index.html
#	wkhtmltopdf index.html index.pdf
#
#index.docx: index.md
#	pandoc --from markdown --to docx -o index.docx index.md
#
#index.txt: index.md
#	pandoc --standalone --smart --from markdown --to plain -o index.txt index.md
#
#clean:
#	rm -f *.html *.pdf *.docx *.txt
