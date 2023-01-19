# Wetube Reloaded

1. 현재 영상을 upload만 해도 비밀번호가 hash 되고 있다. upload를 하면 save() 가 실행되기 때문
2. User.js - 에서 userSChema.pre 에 if (this.isModified(수정할값)) 을 넣어준다.
3. 이렇게 하면 비밀번호가 수정될때 마다 hash 가 된다.
4. getEdit form을 owner(영상을 올린 유저)만 나타나도록 만들자.
5. 영상의 주인이 아니면 접속이 불가능 하게 해야한다.
6. videoController.js - getEdit 변수에 if (video.owner !== req.session.user_id) 비디오 오너가 현재 로그인한 유저의 id와 다르면
7. return res.status(403).redirect("/") 접근 금지 시키고 홈페이지로 돌아가게 한다.
8. 코드를 깔끔히 하기 위해 const {user:{\_id}} = req.session; 을 넣어준다.
9. 주의할점은 자바스크립트는 생김새뿐만 아니라 데이터 형식도 비교한다. (번호가 같아도 데이터 형식이 다르면 다르다고 말한다. )
10. 그리하여 String(video.owner) !== String(\_id) 형식으로 감싸줘야한다.
11. getEdit 뿐만 아니라 postEdit도 넣어서 보호해준다.
12. deleteVideo에서도 수정해줘야한다.
13. deleteVideo에 const video = await Video.findById(id) 를 넣어준다.
14. getEdit, postEdit 에서 했던 코드를 복사해서 넣어준다.
15. 이제 video를 찾으면 owner가 현재 로그인된 유저의 id 와 같은지 확인한다.
16. 일치 하지 않으면 금지하고 홈페이지로 redirect 시킨다.
