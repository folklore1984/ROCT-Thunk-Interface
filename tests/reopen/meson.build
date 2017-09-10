e = executable('kmtreopen', 'kmtreopen.c',
		include_directories : inc,
		link_with : hsakmtlib,
		link_args : '-ldl')

test('hsakmt-reopen', e)
