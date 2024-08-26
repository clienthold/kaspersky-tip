Uploading a file for analysis
==============================

.. code:: python

   def upload(self, filepath: str, silent: bool = False) -> kaspersky_response:

📦 Arguments
*************

- filepath (str): The path to the file to upload.
- silent (bool): Whether a silent scan should be requested.

↩️ Returns
**********

- is_safe (bool): Whether the file is safe or not.
- status (str): The file status.
- filetype (str): The size of the file.
- first_seen (datetime): The first time the file was seen.
- last_seen (datetime): The last time the file was seen.
- hits_count (int): The number of hits the file has.
- threats (list): A list of threats associated with the hash.
- strings (list): A list of strings associated with the hash.

Example of upload file:

.. code:: python

    import kasperskytip

    ks = kasperskytip.kaspersky_tip()
    file = ks.search("C653365657FBF65429AD845D0A0D93106E972ACA929739560FF4B4796BD2BE08")

    print(file.is_safe)
    >>> False

    print(file.status)
    >>> Malware

    print(file.filetype)
    >>> dll x32

    print(file.first_seen)
    >>> 2020-06-10 14:23:00

    print(file.last_seen)
    >>> 2021-06-25 03:23:00

    print(file.hits_count)
    >>> 10

    print(file.threats)
    >>> ['Trojan-Banker.Win32.Cridex.okj']

    print(file.strings)
    >>> ['DD$j@j', '@3|LPkg', '@.reloc', '8l(TPr', 'D$H9D$', 'D$ ludef', '998X+*S', 'FF9i2z{', '@Pm.&t', 'Ddqlt$', 'QQSVj8j@', '9I_\tGv', '&FoA^F9', 'u\x0c9~\x0cu\rj', 'u\x0c9^\x0cu', 'PW5N~<A', '>^@`tw', 'VDD$D$', 'u/9T$ u)', 'Wu\rVVS', ';u\x0ct.;', 'uv\\Wu@', '#:@o\\R', ')`t{.p`k>F', '7rr\x0cuY', ';K+HI$', 'M\x0c;J\x0cr', '< t3<\tt/', 't\rf;1u', '`.rdata', 'u^0"Yo', 'uG\x0cML5F', 'nW0a?W', 'Cu$?)(', 'URPQQh', '$$0L"-', 'uuL$Vr.', 'VFsEpr', '8k^zVS9F', 'nGMF~-', 'fbz4+2`6', 'xn|&;!', 'LLDW|T$$H', '}\x0c;G\x0cv\x0cP', '9D$(rB9|$', 'Pt0$|L$', '999hGlh`', '@\x0c@tDj', ';t$,v-', 'PPPPPWS', 'PPPPPPPP', ';q`>|g', '.gfids', 'x.IvPa', 'c~K.Rd[', 'zSSSSj', '9>t\x0bWV', '@.rsrc', 'j) \x0c%8', 't\x0c;E\x0ct', '|$$t\x0cx', '"#EIzT', 'SCY)\t29', '\\eK5.n', 'PP9E u:PPVWP', 'u\tj\rZf', '_^[ËL$', '8`|FfJr2$o8', 'ilcSII', '9gP)\x0cD', '(iry^]#', 'L$SLNd', ';$܉\x0cNs$', "'`AjZ$", 'LL\\jg%$', 'k\x0cUQPXY]Y[', "]\x0c;3t'", 'Dj^t\x0c9$S', '+/uc$v', 'aUG2,c/&', '7X=}Fj', '$Ct0$D', 'T\tLF2\\', '@.data', ')F9D\tL', '$WLV$tj', 'j Y+ȋE', '^Akx{0Q', '9tZP)%', 't!kl $', '~tmx0>', "U$=4!'", 'f9:t!V', 'u4j\rXSf', '| $@HD', '!This program cannot be run in DOS mode.', '=;a<uG', '^L1\x0b$$', '(SUVWk', '3\x0c8_^]']
