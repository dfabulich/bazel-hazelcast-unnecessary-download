genrule(
	name='big',
	outs=['big.bin'],
	cmd='dd if=/dev/urandom of=$@ count=100 bs=1048576',
)

genrule(
	name='x',
	srcs=['big'],
	outs=['x.txt'],
	cmd='echo hello > $@',
)

genrule(
	name='y',
	srcs=['x'],
	outs=['y.txt'],
	cmd='cp $(location x) $@',
)