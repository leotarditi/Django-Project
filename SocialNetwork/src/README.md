## Setup

- `virtualenv social`
- `cd social`
- Create src folder
- `cd src` & `django-admin startproject bffbook`
- `cd bfbook`
- `python manage.py migrate`
- `python manage.py createsuperuser`
- `python manage.py runserver`
- Into the browser
- Change setting.py & Create templates folder
- Define STATICFILES_DIRS & Create static_project folder
- Define STATIC_ROOT, MEDIA_URL & MEDIA_ROOT
- Import settings & static in url.py
- `python manage.py collectstatic`
- Login with superuser

## Profiles Models

- profiles (Profile, Relationship)
- `python manage.py startapp posts` & `python manage.py startapp profiles`
- Change INSTALLED_APPS (settings)
- Create class Profile
- Import in admin.py
- `python manage.py makemigrations` & `python manage.py migrate`
- Create util.py
- Change __init__.py & app.py
- Create signal.py
- Create Realtionship class
- Import in admin.py
- `python manage.py makemigrations` & `python manage.py migrate`
- Add post_save_add_to_friends (signals)

## Views & Templates

- Create views.py (bffbook) & import in urls.py
- Create folder main (home.html, navbar.html) & base.html
- Create main.js & style.css (static_project)
- Create template folder profile (myprofile.html) & import in views.py
- Create urls.py (profiles) & Add in bffbokk
- Add get_friends & get_friends_no functions in models.py (profiles)
- Create forms.py (profiles) & import in views.py
- Create confirm in views.py (use valid)
- Add semanti-ui in myprofile.html
- Change style.css (add .mymodel & .mt-5)

## Posts Models

- Create class Post in models
- Create class Comment in models
- Create class Like in models 
- Add classes in admin.py
- `python manage.py makemigrations` & `python manage.py migrate`
- Change init.py and app.py
- Add number of post, like given & received in myprofile.html
- Add post_comment_create_and_list_view (posts)
- Create urls.py (posts) & import
- Create folder templates (main.html)
- Add style to main.html
- Create like_unlike_post  (posts views)
- Add funtionality button like
- Create forms.py for create new comments
- Add PostModelForm in the post view
- Add form in the main.html
- Create CommentModelForm in forms.py
- Add c_form in views & main
- Change main.html
- Add new style in style.css (.mb-5, .bwhite-lg, .bwhite-sn, .comment-box)
- Create PostDeleteViews (DeleteViews) in views.py & add new path
- Create PostUpdateViews (UpdateViews) in views.py & add new path
- Create update.html & confirm_del.html

## Manager models

- Create RelationshipManager (invitation_recived)
- Add invites_recived_new in views.py & register views (urls.py)
- Create my_invites.html
- Create ProfileManager (get_all_profiles_to_invite & get_all_profiles)
- Add profiles_list_view &  invite_profiles_list_view in views.py & register views (urls.py)
- Create profile_list.html & to_invite_list.html
- Create ProfileListView(ListView)
- Add ui semantic to profile_list & button (add, waiting & remove)
- Create function view send_invatation & remove_from_friends
- Add functionality to button 
- Add pre_delete signal & Create pre_delete_remove_from_friends
- Change style.css (.w-big)
- Add function accept_invatation & reject_invatation in views
- Create my_invites.html
- Add acept & reject button in my_invites
- Add functionality in button
- Create class ProfileDetailView(DetailView) & import
- Create detail.html
- Change models.py (profiles)
- Add funtionality to See Profile button

## Ajax

- Add Ajax to like_dislike_button (views.py)
- Change Like Button in main.html
- Add like-form event with script

## NavBar

- Add login_requiered
- Add LOGIN_URL in settings
- Add LoginRequieredMixin
- Add functionality to navbar

## Context

- Create context_processors in profiles
- Add context_proccesors in settings
- Add Profile Picture in navbar 
- Add counter to invitation

## Authentication & registration

- `pip install django-allauth`
- Use intruccion to: django-allauth Documentation
- `python manage.py migrate`
- Go to allauth/templates, copy account & paste in social/src/templates
- Add LOGIN_REDIRECT_URL
- Change logout.html, login.html, password_reset.html & signup.html
- Change setting.py
- Add logout in navbar