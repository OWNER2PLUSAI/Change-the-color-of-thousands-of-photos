# Change-the-color-of-thousands-of-photos




### import library we need it

    import cv2 as  cv
    import os
    import time


## be careful for set path beacuse i use path in diffrent place
### Desired photo input path

    path = "INPUT"

###  Desired photo output path

    new_path = "OUTPOT"

# this show u all of image names u have in directory


    os.listdir(path)[0 :len(os.listdir(path))]



    for image in os.listdir(path)[0 :len(os.listdir(path))]:
  
    #      i use path |there|   
    img = cv.imread(path + "/{} ".format(image))
    
    #change colorformat u want      |......there....|     
        img_gray = cv.cvtColor(img, cv.COLOR_BGR2GRAY)
        imag_resize = cv.resize(img_gray, (800, 600))
        cv.imwrite(new_path + "/{} ".format(image), img_gray)
        print(new_path + "/{} ".format(image), "   :::::DONE ")



    #     THIS FOR TEST FOR img_gray.... NOT IMPORTANT .....
    #     imag_resize = cv.resize(img_gray, (800, 600))
    #     cv.imshow(path + "/{} ".format(image) , imag_resize)
    #     cv.waitKey(4000)
    #     cv.destroyAllWindows()
    #     time.sleep(1)
