# Lab 1: Matej Gradoš

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

   https://github.com/mathieux95/digital-electronics-1/blob/295a5cabb7a3af85f5d97ae07c0e54535faae235/labs/01-gates/equations.png

2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of demorgan is
begin
    f_org_o  <= (not(b_i) and a_i) or (not(c_i) and not(b_i));
    f_nand_o <= ((b_i nand b_i) nand a_i) nand ((c_i nand c_i) nand (b_i nand b_i));
    f_nor_o  <= ((b_i nor (a_i nor a_i)) nor (c_i nor b_i))nor((b_i nor (a_i nor a_i)) nor (c_i nor b_i));
end architecture dataflow;
```

3. Complete table with logic functions' values:

| **c** | **b** |**a** | **f(c,b,a)_ORG** | **f(c,b,a)_NAND** | **f(c,b,a)_NOR** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1| 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   https://github.com/mathieux95/digital-electronics-1/blob/b6297501a74088afd188047ebc77e217966f39bc/labs/01-gates/Screenshot%20with%20simulated%20time%20waveforms.png

2. Link to your public EDA Playground example:

   [https://www.edaplayground.com/...](https://www.edaplayground.com/...)
