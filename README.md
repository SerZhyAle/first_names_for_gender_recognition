# first_names_for_gender_recognition
Catalog of First Names to recognise the gender (sex)

CREATE TABLE first_names
(
    id                 int UNSIGNED AUTO_INCREMENT PRIMARY KEY COMMENT 'Uniq record ID -bigint',

    name               varchar(255)                     NOT NULL COMMENT 'Name -varchar(255)',
    name_upper         varchar(255)                     NOT NULL COMMENT 'Upper case name -varchar(255)',
    name_lower         varchar(255)                     NOT NULL COMMENT 'Lower case name -varchar(255)',
    name_ascii         varchar(255) CHARACTER SET ascii NOT NULL COMMENT 'ASCII characters name -varchar(255)',
    name_length        tinyint                          NOT NULL COMMENT 'Length of Name -tinyint',
    like_pattern       varchar(255)                     NOT NULL COMMENT 'LIKE pattern -varchar(255)',
    is_male            tinyint(1)                       NULL COMMENT 'Is Male Name NULL for surnames -tinyint(1)',
--    is_surname   tinyint(1) COMMENT 'Is surname (family name)',
    country_code       char(2)                          NULL COMMENT 'Country alpha code -char(2)',
    frequency          int                              NULL COMMENT 'Frequency in internet database -int',
    domestic_frequency int                              NULL COMMENT 'Frequency in our database -int',
    source_code        char(20)                         NULL COMMENT 'Source Code -char(20)',

    #row activity fields
    created_at         timestamp                        NOT NULL DEFAULT CURRENT_TIMESTAMP COMMENT 'Created -timestamp',
    updated_at         timestamp                        NULL     DEFAULT NULL ON UPDATE CURRENT_TIMESTAMP COMMENT 'Updated -timestamp'
) COMMENT 'Common names';

