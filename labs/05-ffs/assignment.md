# Lab 5: Radim Macho

### Preparation tasks

**D-type FF**
| **clk** | **d** |**q(n)** | **q(n+1)** | **Comments** |
| :-: | :-: | :-: | :-: | :-: |
| up | 0 | 0 | 0 | q(n+1) has the same level as d |
| up | 0 | 1 | 0 | q(n+1) has the same level as d |
| up | 1 | 0 | 1 | q(n+1) has the same level as d |
| up | 1 | 1 | 1 | q(n+1) has the same level as d |

**JK-type FF**
| **clk** | **j** | **k** | **q(n)** | **q(n+1)** | **Comments** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| up | 0 | 0 | 0 | 0 | No change |
| up | 0 | 0 | 1 | 1 | No change |
| up | 0 | 1 | 0 | 0 | Reset |
| up | 0 | 1 | 1 | 0 | Reset |
| up | 1 | 0 | 0 | 1 | Set |
| up | 1 | 0 | 1 | 1 | Set |
| up | 1 | 1 | 0 | 1 | Toggle |
| up | 1 | 1 | 1 | 0 | Toggle |

**T-type FF**
| **clk** | **t** |**q(n)** | **q(n+1)** | **Comments** |
| :-: | :-: | :-: | :-: | :-: |
| up | 0 | 0 | 0 | No change |
| up | 0 | 1 | 1 | No change |
| up | 1 | 0 | 1 | Toggle |
| up | 1 | 1 | 0 | Toggle |

### Flip-flops

1. Listing of VHDL architecture for T-type flip-flop. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture Behavioral of t_ff_rst is
    signal s_q : std_logic;
begin
    --------------------------------------------------------
    -- p_t_ff_rst:
    -- T type flip-flop with a high-active sync reset,
    -- rising-edge clk.
    -- q(n+1) = t./q(n) + /t.q(n)
    --------------------------------------------------------
    p_t_ff_rst : process(clk)
    begin

        -- WRITE YOUR CODE HERE

    end process p_t_ff_rst;

    q     <= s_q;
    q_bar <= not s_q;
end architecture Behavioral;
```

2. Screenshot with simulated time waveforms. Try to simulate both flip-flops in a single testbench with a maximum duration of 200 ns, including reset. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![your figure]()

### Shift register

1. Image of the shift register block schematic. The image can be drawn on a computer or by hand. Always name all inputs, outputs, components and internal signals!

   ![your figure]()