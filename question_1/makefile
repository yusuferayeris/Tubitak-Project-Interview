ORBITER= ../../orbiter/src/apps/orbiter/orbiter.out
PDFLATEX=pdflatex
OPEN=open
DC:
	$(ORBITER) -v 3 \
		-define yusuf -graph \
			-yusuf_eray_double_cover 7 \
		-end \
		-with yusuf -do \
		-graph_theoretic_activity \
			-properties \
		-end \
		-with yusuf -do \
		-graph_theoretic_activity \
			-automorphism_group \
		-end \
		-with yusuf -do \
		-graph_theoretic_activity \
			-eigenvalues \
		-end \
		-with yusuf -do \
		-graph_theoretic_activity \
			-eigenvalue_report \
		-end \
		-with yusuf -do \
		-graph_theoretic_activity \
			-export_csv \
		-end	
	$(PDFLATEX) yusuf_eray_double_cover_7_report.tex
	$(OPEN) yusuf_eray_double_cover_7_report.pdf 
	$(PDFLATEX) yusuf_eray_double_cover_7_eigenvalues.tex
	$(OPEN) yusuf_eray_double_cover_7_eigenvalues.pdf