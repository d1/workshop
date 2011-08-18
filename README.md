
This repo contains several slide presentations for use during the Railsbridge Open Workshops (specifically the Ruby For Women Workshops).

Not all presentations are ready to be shown yet!

# Quick Start

	# install the workshop materials
	git clone git://github.com/railsbridge/workshop.git
	cd workshop

	# install the gems
	gem install bundler
	bundle install

	# run the standard presentation
	rake showoff serve

This will launch a local Sinatra server on port 9090. Open your browser to `localhost:9090`. On a Mac you can run:

    open http://localhost:9090

Use arrow keys to navigate slides. Press '?' to see a help window with more key commands.

# Showoff Versions

We use a Ruby app called `showoff` to generate and serve the workshop slides.

Alex has been improving showoff; until his latest patches get accepted and released, you will have to use his version. If you use Bundler and Rake (as in "Quick Start" above) it should grab and use the correct version.

Otherwise, you'll want to download and install it, as follows:

    git clone git://github.com/alexch/showoff.git
    cd showoff
    bundle install --without optional
    rake gem:install

# Running a single presentation

The proper way to use showoff is to run a set of slides as described in the `showoff.json` file in the project root directory.

However, if you want to run a subdirectory's worth of slides only, you have two choices.

For example, if you want to run the "Teacher Training" presentation, which lives in the `teachers` directory, you can run it from the project root directory:

    rake showoff serve teachers

# Running several presentations in a row

You can create a custom presentation out of any combination and ordering of the section directories by creating your own `showoff.json` file. See `nyc.json` for an example -- it's the same as the standard `showoff.json` but inserts NY-specific resources after the Welcome section.

    rake showoff serve --pres_file nyc.json

# Editing slides

Slides are in [Markdown](http://daringfireball.net/projects/markdown/syntax) format. Showoff will read all `.md` files in alphabetical order.

You can also add custom `.css`, `.scss`, and `.js` files, which will get imported into all slide sections.

Images should be in the same directory as the slide that references them.

Workshops should edit the `current.md` file to contain accurate schedule and sponsor information.

# Printing slides

Try this: first `gem install pdfkit`, then visit

    http://localhost:9090/pdf

but I make no guarantees!

# Support

Email <mailto:railsbridge-workshops@googlegroups.com>

# LICENSE

This project is under an open source license. We're not sure exactly which one... probably MIT.

Gill Sans is under copyright. It's a great slide font and it comes with all recent Macs (and Gill Sans MT comes with MS Office).
But it might not be on the instructor's machine so I checked in a zip file. This was probably the wrong thing to do.

Here is Gill Sans licensing info
  <http://www.fontslive.com/font/gill-sans-family.aspx>
  <http://www.ascendercorp.com/font/gill-sans/>

"The Gill Sans stack should work on most all computers. Gill Sans comes on all
Macs and Gill Sans MT is installed with Microsoft Office, and Calibri (which
is a good stand-in for Gill Sans) is one the core Vista fonts and is installed
with both Office Windows and Office Mac. And lastly, if all else fails, use
Trebuchet" - <http://www.artsiteframework.com/guide/fontstacks.php> -- the stack
he's talking about is

    "Gill Sans", "Gill Sans MT", GillSans, Calibri, "Trebuchet MS", sans-serif

Perhaps we should replace it with a free font like SansBetween
  http://manfred-klein.ina-mar.com/
  http://manfred-klein.ina-mar.com/fonts/2008-02/SansBetween-MAC.zip
  http://manfred-klein.ina-mar.com/fonts/2008-02/SansBetween-PC.zip
