
# Data Propagation Report

- **STAT1** : Number of instructions that hit unique coverpoints and update the signature.
- **STAT2** : Number of instructions that hit covepoints which are not unique but still update the signature
- **STAT3** : Number of instructions that hit a unique coverpoint but do not update signature
- **STAT4** : Number of multiple signature updates for the same coverpoint
- **STAT5** : Number of times the signature was overwritten

| Param                     | Value    |
|---------------------------|----------|
| XLEN                      | 32      |
| TEST_REGION               | [('0x80000104', '0x80000130')]      |
| SIG_REGION                | [('0x80002070', '0x80002090', '8 words')]      |
| COV_LABELS                | ecall      |
| TEST_NAME                 | /scratch/git-repo/incoresemi/riscof/riscof_work/ecall.S/ecall.S    |
| Total Number of coverpoints| 1     |
| Total Coverpoints Hit     | 1      |
| Total Signature Updates   | 6      |
| STAT1                     | 1      |
| STAT2                     | 0      |
| STAT3                     | 0     |
| STAT4                     | 5     |
| STAT5                     | 0     |

## Details for STAT2:

```


```

## Details of STAT3

```


```

## Details of STAT4:

```
Last Coverpoint : ['opcode : ecall']
Last Code Sequence : 
	-[0x80000114]:ecall
Current Store : [0x80000358] : sw t2, 4(t1) -- Store: [0x8000207c]:0x0000000B




Last Coverpoint : ['opcode : ecall']
Last Code Sequence : 
	-[0x80000114]:ecall
Current Store : [0x80000370] : sw t4, 8(t1) -- Store: [0x80002080]:0x00000108




Last Coverpoint : ['opcode : ecall']
Last Code Sequence : 
	-[0x80000114]:ecall
Current Store : [0x80000408] : sw t2, 12(t1) -- Store: [0x80002084]:0x00000000




Last Coverpoint : ['opcode : ecall']
Last Code Sequence : 
	-[0x80000114]:ecall
Current Store : [0x80000120] : sw zero, 0(ra) -- Store: [0x80002070]:0x00000000




Last Coverpoint : ['opcode : ecall']
Last Code Sequence : 
	-[0x80000114]:ecall
Current Store : [0x80000124] : sw sp, 4(ra) -- Store: [0x80002074]:0x11111111





```

## Details of STAT5:



## Details of STAT1:

- The first column indicates the signature address and the data at that location in hexadecimal in the following format: 
  ```
  [Address]
  Data
  ```

- The second column captures all the coverpoints which have been captured by that particular signature location

- The third column captures all the insrtuctions since the time a coverpoint was
  hit to the point when a store to the signature was performed. Each line has
  the following format:
  ```
  [PC of instruction] : mnemonic
  ```
- The order in the table is based on the order of signatures occuring in the
  test. These need not necessarily be in increasing or decreasing order of the
  address in the signature region.

|s.no|        signature         |     coverpoints     |         code          |
|---:|--------------------------|---------------------|-----------------------|
|   1|[0x80002078]<br>0x0000008F|- opcode : ecall<br> |[0x80000114]:ecall<br> |
