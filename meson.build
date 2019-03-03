project('bin2c', ['c'], 
         version       : '1.0.0',  
         license       : ['PD'],
         meson_version : '>= 0.49.0')




system     = build_machine.system()
cpu        = build_machine.cpu()
cpu_family = build_machine.cpu_family()

cc    = meson.get_compiler('c')
cc_id = cc.get_id() 




if system not in ['windows']
    error('Script (meson.build) not prepared for your platform yet.')
endif

if system == 'windows' and cc_id not in ['msvc']
    error('Script (meson.build) not prepared for your compiler yet.')
endif




bin2c_cmd = executable('bin2c' 
                       ,sources : ['bin2c.c']
                       ,install : true)




install_data(['LICENSE.txt'],
               rename : ['LICENSE.PD'],
               install_dir : 'share/licenses/bin2c')

install_data(['readme.txt'],
               rename : ['README'],
               install_dir : 'share/docs/bin2c')