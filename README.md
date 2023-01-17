# Wetube Reloaded

1. watch.pug 에서 if video.ower 와 loggedInUser.\_id 가 일치하면 Edit video 와 delete video 를보여주게한다.
2. videoSchema에 owner를 추가한다. reference를 User로 추가하고 import 한다. video와 user가 연결된다.
3. postUpload 에 owner:\_id 를 추가한다.
4. watch 안에 owner 변수를 추가한다. User.findById 를 넣어준다. 여기선 이미 서로 연결됨
5. watch.pug 에서 uploaded by owner.name 을 해준다.
