# The list of lectures.

LECTURES= GettingStarted

################### Configuration ##################.


SLIDE_FORMAT=revealjs    # The slide format to use.

REVEAL_VERSION=2.6.2     # Version of revel to use.
REVEAL_THEME=solarized   # Theme of revel to use.


################ Hacker zone ################################


REVEL_OPTS=-V theme=${REVEAL_THEME} \
	   -V revealjs-url=reveal.js-${REVEAL_VERSION} \
	   --slide-level=2 \
	   --include-in-header tweak.css

HTML_OPTS= -t ${SLIDE_FORMAT} ${REVEL_OPTS}

HTML=$(addsuffix .html, ${LECTURES})


.PHONY: all clean

all: ${HTML}

clean:
	rm -f ${HTML}

%.html: %.md tweak.css
	pandoc ${HTML_OPTS} -s $< -o $@
