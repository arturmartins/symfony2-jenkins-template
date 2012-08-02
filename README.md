Symfony2 Jenkins Template
=========================

Based on Sebastian Bergmann's template: http://github.com/sebastianbergmann/php-jenkins-template

### Installation

Follow the installation steps from [Jenkins PHP](http://jenkins-php.org) for installing needed deendencies (ignore the xml files from there) and follow with these particular steps:

1. Clone this repository:
    git clone git://github.com/arturmartins/symfony2-jenkins-template.git

2. Move the jenkins folder to `[SYMFONY2_ROOT]/app/Resources/` inside your Symfony2 project.

3. Move `build.xml` to the root folder of your Symfony2 application.

4. Move `phpunit.xml` to `[SYMFONY2_ROOT]/app` folder or update the existing one. The `logging` node is needed!

5. Add th [symfony2-coding-standards](https://github.com/opensky/Symfony2-coding-standard) in your phpcs naming it as `Symfony2` or edit the phpcs target on build.xml with the right parameters for your envirement.

You can customize the configuration as you want, this works fine with me :)

### How to add this to your jenkins?

Add an "Execute shell" build step with the following lines:
git clone https://github.com/arturmartins/symfony2-jenkins-template.git sf2-jt
cp -a sf2-jt/jenkins app/Resources
cp -a sf2-jt/build.xml build.xml
cp -a sf2-jt/phpunit.xml app/phpunit.xml
rm -rf sf2-jt

 