active_admin_sidebar
====================

easy change sidebar position with activeadmin


1) change sidebar position dynamically with before_filter

  # app/admin/posts.rb
  ActiveAdmin.register Post do
    before_filter :sidebar_left!
  end

  # app/admin/comments.rb
  ActiveAdmin.register Comment do
    before_filter :sidebar_right!
  end



2) move sidebar to left within all resource


  # == Controller Filters
  #
  # You can add before, after and around filters to all of your
  # Active Admin resources from here.
  #
  config.before_filter :sidebar_left!
