bne t1, t2, label
 - Branch if not equal: Branch to statemetn at labels address if t1 and t2 are not equal

beq t1, t2, label
 - Branch if equal: Branch to statement at label's address if t1 is greater than or equal to t2

bge t1, t2, label
 - Branch if greater than or equal: Branch to statement at label's address if t1 is greater than or equal to t2

blt t1, t2, label
 - Branch if less than: Branch to statement at label's address if t1 is less than t2

ecall
 - Issue a system call: Execute the system call specified by a value in a7

