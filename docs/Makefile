# Minimal makefile for Sphinx documentation
#

# You can set these variables from the command line.
SPHINXOPTS    =
SPHINXBUILD   = sphinx-build
SPHINXPROJ    = Neuron-Matrix
SOURCEDIR     = source
BUILDDIR      = ../../neuron-matrix-docs
PDFBUILDDIR   = /tmp/$(SPHINXPROJ)
PDF           = ../manual.pdf


# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: help Makefile

latexpdf:
	$(SPHINXBUILD) -M latexpdf $(SOURCEDIR) $(PDFBUILDDIR)
	cp $(PDFBUILDDIR)/latex/$(SPHINXPROJ).pdf $(PDF)

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)
