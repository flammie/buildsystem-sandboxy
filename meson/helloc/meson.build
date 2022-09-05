project('hello', 'c', version : '0.0.0')
executable('helloc', 'hello.c')

conf = configuration_data()
conf.set_quoted('VERSION', '0.0.0')
configure_file(output : 'config.h',
               configuration : conf)

