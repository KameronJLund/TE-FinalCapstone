
# TE Gram initial layout design
### Feel free to change as needed. Photo assets stored in vue/src/components/

# Front End
## <br> Account page
![FrontEndDesign1](vue\src\resources\FrontEndDesign1.png)

## <br> Home View - Wide Screen
#### Static Nav Bar on top && bottom
![FrontEndDesign2](vue\src\resources\FrontEndDesign2.png)

## <br> Main Desktop View
#### dark vs light mode + pref accent color (green in this case)
#### set amount of columns, infinite rows (rows don't have to line up)
#### click to view post
![MainPageLayout](vue\src\resources\TeGramMainPageLayout.png)

## <br> Mobile
#### Static Nav Bar on top && bottom
#### Heart = like / Triangle = favorite
![FrontEndDesign3](vue\src\resources\FrontEndDesign3.png)

# <br> Backend
## <br> Database
### User/Login Table
- userId
- username
- pass

### <br> User-Account Relational Table
- userId
- accountId

### <br> Account Details Table
- accountId
- profilePic (url? or id?)
- bio

### <br> Created Photos Table
- accountId
- photoID

### <br> Photo Details Table
- photoId
- imgUrl
- caption
- createdDate
- isPrivate

### <br> Likes Table
- accountId
- photoId

### <br> Favorites Table
- accountId
- photoId


### <br> Photo Comments
- photoId
- commentId

### <br> Comments Table
- commentId
- comments
- accountID

# <br> Endpoints
- GET All photos not private (home)
- GET Photo description + comments
- Your account
    - GET Account details
    - PUT Account details
    - GET All photos incl private
- Other account
    - GET Account details
    - GET All photos
- GET All favorites photos
- POST photo description 
- POST comments 
