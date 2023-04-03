# Project 6 - *Be Real.*

Submitted by: **XiaoyangJin**

**Name of your app** is an app that allows users to post with pictures chosen from album or taken by camera

Time spent: **15** hours spent in total

## Required Features

The following **required** functionality is completed:

- [x] User can launch camera to take photo instead of photo library
- [x] User session persists when application is closed and relaunched
- [x] Users are able to log out and return to sign in page
- [x] Users are NOT able to see other photos until they upload their own	
 
The following **optional** features are implemented:

- [x] User receive notifcation when it is time to post
- [ ] Users can make comments and view comments in posts	

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app functionality!
I implemented the limited time function but forget to post yesterday, so it is not so apparent in the gif, but here's the related code, hope that can make some sence:
        let yesterdayDate = Calendar.current.date(byAdding: .day, value: (-1), to: Date())!
        let query = Post.query()
            .include("user")
            .order([.descending("createdAt")])
            .where("createdAt" >= yesterdayDate)
            .limit(10)

## Video Walkthrough

Here's a walkthrough of implemented user stories:

https://imgur.com/FX7H9OW.gif

## Notes

Describe any challenges encountered while building the app.
Just an odd error when I first build my project on my own device, but the error fixed automatically after I unplugged my phone from my computer.

## License

    Copyright [2023] [XiaoyangJin]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
