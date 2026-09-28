ORBITER= ../../orbiter/src/apps/orbiter/orbiter.out
PDFLATEX=pdflatex
OPEN=open

Q2:
	$(ORBITER) -v 3 \
		-define F9 -finite_field -q 9 -end \
		-define P9 -projective_space -n 2 -field F9 -v 0 -end \
		-define C9 -quartic_curve -space P9 -by_normal_form "6,3,4,6,2,5" -end\
		-define F11 -finite_field -q 11 -end \
		-define P11 -projective_space -n 2 -field F11 -v 0 -end \
		-define C11 -quartic_curve -space P11 -by_normal_form "8,5,3,2,10,7" -end\
		-define F17 -finite_field -q 17 -end \
		-define P17 -projective_space -n 2 -field F17 -v 0 -end \
		-define C17 -quartic_curve -space P17 -by_normal_form "2,7,16,3,9,4" -end\
		-with C9 -do \
			-quartic_curve_activity \
				-report \
		-end \
		-with C11 -do \
			-quartic_curve_activity \
				-report \
		-end \
		-with C17 -do \
			-quartic_curve_activity \
				-report \
		-end \
		-print_symbols
	$(PDFLATEX) quartic_curve_by_normal_form_q9_report.tex
	$(PDFLATEX) quartic_curve_by_normal_form_q11_report.tex
	$(PDFLATEX) quartic_curve_by_normal_form_q17_report.tex
