import os
import shutil
import re
import fnmatch

source = 'C:/Users/TEST/Desktop/64/out'
src_files = os.listdir(source)
print (len(fnmatch.filter(os.listdir(source), '*.csv')))

dest_Mama_36 = 'Z:/Schedules/Mama'
dest_Mama_37 = 'D:/Schedules/Mama'

dest_Mult_36 = 'Z:/Schedules/Mult'
dest_Mult_37 = 'D:/Schedules/Mult'

dest_MyPlanet_36 = 'Z:/Schedules/MyPlanet'
dest_MyPlanet_37 = 'D:/Schedules/MyPlanet'

dest_NAYKA_36 = 'Z:/Schedules/NAYKA'
dest_NAYKA_37 = 'D:/Schedules/NAYKA'

dest_NST_36 = 'Z:/Schedules/NST'
dest_NST_37 = 'D:/Schedules/NST'

dest_Techno24_36 = 'Z:/Schedules/Techno24'
dest_Techno24_37 = 'D:/Schedules/Techno24'

for file_name in src_files: 
    if re.search(r'^20[1-9]\d-[01]\d-[0-3]\d_Мама\.csv$',file_name):
        src = os.path.join(source, file_name)
        dst36 = os.path.join(dest_Mama_36, file_name)
        dst37 = os.path.join(dest_Mama_37, file_name)
        shutil.copy(src, dst36)
        shutil.copy(src, dst37)
        print ('Скопировано Мама')
	
    elif re.search(r'^20[1-9]\d-[01]\d-[0-3]\d_Мульт\.csv$',file_name):
        src = os.path.join(source, file_name)
        dst36 = os.path.join(dest_Mult_36, file_name)
        dst37 = os.path.join(dest_Mult_37, file_name)
        shutil.copy(src, dst36)
        shutil.copy(src, dst37)
        print ('Скопировано Мульт')
   
    elif re.search(r'^20[1-9]\d-[01]\d-[0-3]\d_МП\.csv$',file_name):
        src = os.path.join(source, file_name)
        dst36 = os.path.join(dest_MyPlanet_36, file_name)
        dst37 = os.path.join(dest_MyPlanet_37, file_name)
        shutil.copy(src, dst36)
        shutil.copy(src, dst37)
        print ('Скопировано Моя планета')

    elif re.search(r'^20[1-9]\d-[01]\d-[0-3]\d_Наука\.csv$',file_name):
        src = os.path.join(source, file_name)
        dst36 = os.path.join(dest_NAYKA_36, file_name)
        dst37 = os.path.join(dest_NAYKA_37, file_name)  
        shutil.copy(src, dst36)
        shutil.copy(src, dst37)
        print ('Скопировано Наука')
    
    elif re.search(r'^20[1-9]\d-[01]\d-[0-3]\d_НСТ\.csv$',file_name):
        src = os.path.join(source, file_name)
        dst36 = os.path.join(dest_NST_36, file_name)
        dst37 = os.path.join(dest_NST_37, file_name)  
        shutil.copy(src, dst36)
        shutil.copy(src, dst37)
        print ('Скопировано НСТ')

    elif re.search(r'^20[1-9]\d-[01]\d-[0-3]\d_Т24\.csv$',file_name):
        src = os.path.join(source, file_name)
        dst36 = os.path.join(dest_Techno24_36, file_name)
        dst37 = os.path.join(dest_Techno24_37, file_name)  
        shutil.copy(src, dst36)
        shutil.copy(src, dst37)
        print ('Скопировано T24')
    else:
        print ('Ничего не вышло c ', file_name)

os.system ('pause')
