Heroku buildpack: Perl
======================

This is a Heroku buildpack that runs any PSGI based web applications using Starman.

Usage
-----

Example usage:

    $ git clone https://github.com/OTRS/otrs.git
    $ cd otrs
    $ vi cpanfile
        requires 'Archive::Tar';
        requires 'Crypt::Eksblowfish::Bcrypt';
        requires 'Crypt::SSLeay';
        requires 'Date::Format';
        requires 'DBI';
        requires 'DBD::mysql';
        requires 'Encode::HanExtra';
        requires 'IO::Socket::SSL';
        requires 'JSON::XS';
        requires 'List::Util::XS';
        requires 'LWP::UserAgent';
        requires 'Mail::IMAPClient';
        requires 'IO::Socket::SSL';
        requires 'Net::DNS';
        requires 'Net::LDAP';
        requires 'Net::SSL';
        requires 'PDF::API2';
        requires 'Compress::Zlib';
        requires 'Text::CSV_XS';
        requires 'Time::HiRes';
        requires 'XML::Parser';
        requires 'YAML::XS';

    $ mv Kernel/Config.pm.dist Kernel/Config.pm
    $ mv Kernel/Config/GenericAgent.pm.dist Kernel/Config/GerericAgent.pm

    Change Home Directory

    $ vi Kernel/Config.pm

    $Self->{Home} = '/home/vcap/app';

    Configure mysql service on Bluemix page

    $ cf push your_app_name -b https://github.com/dokechin/heroku-buildpack-otrs.git

    Access installer url
      http://your_app_name.mybluemix.net/installer.pl

    Configure OTRS MySQL setting by Bluemix MySQL Credentials.
      
      Select the Install type "Use an existing database for OTRS" 

      User     is /mysql-5.5/credentials/user
      Password is /mysql-5.5/credentials/password
      Host     is /mysql-5.5/credentials/host:/mysql-5.5/credentials/port 
      Database name is /mysql-5.5/credentials/name
 
