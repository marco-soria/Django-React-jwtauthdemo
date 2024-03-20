python manage.py shell
from django.contrib.auth.models import User
from base.models import Profile



user1 = User.objects.create_user(username='sam', password='sam')

profile1 = Profile.objects.create(
    user=user1,
    first_name='Sam',
    last_name='Smith',
    email='sam@gmail.com'
)


user2 = User.objects.create_user(username='tim', password='tim')

profile2 = Profile.objects.create(
    user=user2,
    first_name='Tim',
    last_name='Allen',
    email='tim@gmail.com'
)