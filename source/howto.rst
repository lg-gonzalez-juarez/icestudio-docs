.. sec-howto

How to...
=========

Create a project
----------------

1. Create a new project

   Go to **Edit > New project**, write your project's name and press OK.

2. Add your blocks

 1. Code blocks

    Click on **basic > code**, add the code ports. Input and output ports are separated by a space. Port names are separated by a comma. E.g.: ``a,b c``.

    This block contains a text editor to write your module verilog code. Module header and footer are not required.

 2. Info blocks

    Click on **basic > info**.

    This block contains a text editor to add comments about the project.

 3. Input/Output blocks

    Click on **basic > input** or **basic > output**, write the block's name and press OK.

    These blocks contain a FPGA pin selector depending on the selected board.

 4. Bit blocks

    Click on **bit > 0** or **bit > 1**.

    These blocks are low and high logic drivers.

 5. Config block

    Click on **config > Input-config**.

    This block must be connected to input ports in order to configure a pull up.

 6. Logic blocks

    Go to the **logic** menu and select a logic gate.

3. Connect your blocks

4. Select your board

   Go to **Boards** menu and select **Icezum**, **iCEstick** or **Go board**.

5. Set FPGA I/O pins

   Select all Input/Output blocks' pins.

6. Save the project

   Go to **Edit > Save**:

   It will be saved as **.ice** file.


Upload a bitstream
------------------

1. Open a project

   Go to **Edit > Open project** and select a **.ice** file.

2. Verify the project

   Go to **Tools > Verify**.

   This option checks the generated verilog code using ``apio verify``.

3. Build the project

   Go to **Tools > Build**.

   This option generates a bitstream using ``apio build``.

4. Upload the project

   Connect your FPGA board and press **Tools > Upload**. This option uses ``apio upload``.


.. note::

  If the FPGA toolchain is not installed, it will be installed automatically when any tool is pressed.


Create a block
--------------

1. Open a project

   Go to **Edit > Open project** and select an **.ice** file.

2. Verify the project

3. Export the project as block

   Go to **Edit > Export as block**.

   It will be saved as **.iceb** file.


.. note::

  Input/Output blocks will become new Block I/O pins.


Use a custom block
------------------

1. Open or create a new project

2. Import the custom block

   Go to **Edit > Import block** and select an **.iceb** file.