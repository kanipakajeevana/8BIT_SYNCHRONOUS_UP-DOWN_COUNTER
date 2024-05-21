# 8BIT_SYNCHRONOUS_UP-DOWN_COUNTER
![image](https://github.com/kanipakajeevana/8BIT_SYNCHRONOUS_UP-DOWN_COUNTER/assets/170450203/4ed2984f-780f-46a9-aac8-492b7e0d400a)

# Here is a diagram showing the circuit in the "up" counting mode
![image](https://github.com/kanipakajeevana/8BIT_SYNCHRONOUS_UP-DOWN_COUNTER/assets/170450203/c6857352-fa50-4573-8e37-d5f4df623d8f)

# Here, shown in the "down" counting mode
![image](https://github.com/kanipakajeevana/8BIT_SYNCHRONOUS_UP-DOWN_COUNTER/assets/170450203/5d6bea60-7a17-49b8-a226-27d25b2f2a00)
# PROGRAM
library IEEE;

use IEEE.STD_LOGIC_1164.ALL;

use IEEE.STD_LOGIC_ARITH.ALL;

use IEEE.STD_LOGIC_UNSIGNED.ALL;

entity updn is

    Port ( clk : in STD_LOGIC;
    
           clr : in STD_LOGIC;
           
           updown : in std_logic;
           
           count : out std_logic_vector (7 downto 0));

end updn;

architecture Behavioral of updn is

signal tmp : std_logic_vector(7 downto 0);


begin

process

begin

wait until clk'event and clk ='1';

if (clr ='1') then

tmp<="00000000";

elsif (updown ='1') then

tmp <= tmp + 1;

else

tmp <= tmp - 1;


end if;

count <= tmp;

end process;

end Behavioral;
# OUTPUT
![image](https://github.com/kanipakajeevana/8BIT_SYNCHRONOUS_UP-DOWN_COUNTER/assets/170450203/32255a2e-ae36-4cff-a95e-6fcea2923de2)




