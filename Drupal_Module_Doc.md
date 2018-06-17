/*How to create custome module*/
1.Create module folder for custom module. However in Drupal has two kind of modules are 
  a. Contributed Module (Customize by developer if require)
  b. Custome Module (created by developer)
2.You should put module folder in following path
  a.sites/all/modules/
  b.sites/all/modules/{custom_module}
3.Now most important step, to create two impotant files
  a.{custom_module}.info /*this file content the information of module info, which give the user understad*/
  b.{custom_module}.module /*This is main coding file, which create/give your application/module functionality. It contain the hook method with special function
  and it will execute when action occur. For example my_example_menu() - my_example denoted module name / hook and _menu denoted as method*/
4.Imporant variable in {custom_module}.info file [ it is store the matadata for theme and module]
  a.name /*Declare the module name and it must be user understandable*/ [require]
  b.description /*description of module*/				[recommended]
  c.core /*current version of drupal*/					[require]
  d.package
  e.dependancies[]=views:views or dependancies[]=panels:panels		{project}:{module}
  f.files[] = path + file_name
  g.configure = admin/config/content/{custom_module}
Note: ';' is use for comment. Whenever you make changes in *.info file, u must clean the site cache
  h.stylesheets[all][] /*call the style sheet, it is single instance*/
  i.scripts[] /**/
  j.php
  h.project status url /*only use in custom module not submitted to drupal.org*/