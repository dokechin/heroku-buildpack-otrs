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

    In the case Bluemix
    $ cf push your_app_name -b https://github.com/dokechin/heroku-buildpack-otrs.git

    Access installer url
    http://your_app_name.mybluemix.net/installer.pl



