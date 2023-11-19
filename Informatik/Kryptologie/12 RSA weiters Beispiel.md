---
tags:
  - Informatik
---
*Marvin Baeumer* **2023-11-17 08:17**

---
$$
\begin{matrix}

4320 & = & 19 & \cdot & 227 & + & 7 \\
19 & = & 7 & \cdot & 2 & + & 5 \\
7 & = & 5 & \cdot & 1 & + & 2 & \\
5 & = & 2 & \cdot & 2 & + & 1 & \\
2 & = & 2 & \cdot & 1& + & 0 &
\end{matrix}
$$
$$
\begin{matrix}
7 & = & 4320 & - & 227 & \cdot  & 19 & \\
5 & = & 19 & - & 7 & \cdot & 2& \\
2 & = & 7 & - & 1 & \cdot & 5 && \\
1 & = & 5 & - & 2 & \cdot & 2 \\
\end{matrix}
$$
$$
\begin{matrix}
\Leftrightarrow & 1 & = & 5 & - & 2 & \cdot & ( & 7 & - & 1 & \cdot & 5 &) \\
&& = & - & 2 & \cdot & 7 & + & 3 & \cdot & 5 & \\ 
&& = & - & 2 & \cdot & 7 & + & 3 & \cdot & ( & 19 & - & 2 & \cdot & 7 & ) & \\
&& = & 3 & \cdot & 19 & - & 8 & \cdot & 7 \\
&& = & 3 & \cdot & 19 & - & 8 & \cdot & ( & 4320 & - & 227 & \cdot & 19 & ) \\
&& = & 1819 & \cdot & 19 & - & 8 & \cdot & 4320&& 
\end{matrix}
$$
$$ d = 1819 $$
$$e = 19$$
### Verschluesselung
$$ 1010^{19} \mod 4453 = 1107 $$
$$1107^{1819} \mod 4453 = 1010$$
