 Example Gallery
========================================

Hello world this is the first chapter!


.. manim:: ManimCELogo

    import manim
    class ManimCELogo(Scene):
        def construct(self):
            banner = ManimBanner().scale(0.5)
            self.add(Title(f"manim version {manim.__version__}").set_color(WHITE))
            self.play(banner.create())
            self.play(banner.expand())
            self.wait()



            
 .. toctree::
    :maxdepth: 2

       code-cells


.. Indices and tables
.. ==================

.. * :ref:`genindex`
.. * :ref:`modindex`
.. * :ref:`search`