project('libscrypt', 'c', version : '0.1.21')

version = meson.project_version()

sources = ['crypto_scrypt-check.c',
'crypto_scrypt-hash.c',
'crypto_scrypt-hexconvert.c',
'crypto_scrypt-nosse.c',
'crypto-mcf.c',
'crypto-scrypt-saltgen.c',
'slowequals.c',
'sha256.c',
'b64.c'
]
inc = include_directories('./')

lib = static_library('scrypt', sources: sources, version: version,
include_directories : inc,
c_args: ['-Wall', '-ffast-math', '-D_FORTIFY_SOURCE=2', '-fstack-protector'],
install: false)

libscrypt_dep = declare_dependency(include_directories : inc,
  link_with : lib)
