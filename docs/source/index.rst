 Example Gallery
========================================

Here is the directive example

.. manim:: ManimCELogo

    import manim
    class ManimCELogo(Scene):
        def construct(self):
            banner = ManimBanner().scale(0.5)
            self.add(Title(f"manim version {manim.__version__}").set_color(WHITE))
            self.play(banner.create())
            self.play(banner.expand())
            self.wait()

.. .. toctree::
..    :maxdepth: 2
..
..       examples


.. Indices and tables
.. ==================

.. * :ref:`genindex`
.. * :ref:`modindex`
.. * :ref:`search`