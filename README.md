# get-signin-activity-report-with-certificate
Shows how to download sign-in activity log on Azure AD using AcquireTokeAsync method with PowerShell

PowerShell �X�N���v�g�� Microsoft Graph API ����яؖ����𗘗p���� Azure AD �̃T�C���C�� �A�N�e�B�r�e�B ���|�[�g�� csv �`���Ŏ擾������@���Љ�܂��B

�����̃L�[�ł͂Ȃ��ؖ�����p�����g�[�N���擾�𐄏����Ă���܂��B�ȉ��Ɉ�A�̎菇�����܂Ƃ߂��܂����̂ŁA�Q�l�Ƃ��Ă���������΍K���ł��B��܂��� 3 �̎菇�ɕ����ĉ���������܂��B

## �F�؂Ɏg�p����ؖ����̏���

����͏�q�̂Ƃ���A�g�[�N���擾�ɏؖ�����p���܂��B����́A����܂ł̕����̃L�[��p������@�����Z�L�����e�B�I�ɋ��͂ł���A���ЂƂ��Ă��������Ă�����@�ł��BCreateAndExportCert.ps1 �����s����ƁA���ȏ����ؖ�������������A���[�U�[�̏ؖ����X�g�A (�l) �Ɋi�[���܂��B����ɁA���J���� .cer �t�@�C���ŃJ�����g �f�B���N�g���ɏo�͂��܂��B


## �����ɕK�v�ȃ��C�u������ nuget �Ŏ擾����X�N���v�g

�ؖ�����p�����g�[�N���擾�����̓��C�u������p���čs���܂��B�����ɕK�v�ȃ��C�u������ nuget �Ŏ擾���܂��BGetAdModuleByNuget.ps1 �����s���������B�{�X�N���v�g�����s����ƁA���s�t�H���_�[�z���Ƀt�H���_�[���ł��AMicrosoft.IdentityModel.Clients.ActiveDirectory.dll �Ȃǂ̃t�@�C�����ۑ�����܂��B

## �T�C���C�� ���O���擾����X�N���v�g

�ؖ����̏�������ю��s�ɕK�v�ȃ��C�u�����̏����������܂�����A�ȉ��̎菇�ŁA�A�v���P�[�V��������уX�N���v�g���������܂��B

�܂��A�ȉ��̃h�L�������g�ɋL�ڂ��ꂽ�菇�ɏ]���āA�A�v���P�[�V������o�^���A"�\���ݒ�����W����" �ɏ]���ăh���C�����ƃN���C�A���g ID ���擾���܂��B

Azure AD Reporting API �ɃA�N�Z�X���邽�߂̑O�����
https://docs.microsoft.com/ja-jp/azure/active-directory/active-directory-reporting-api-prerequisites-azure-portal

�����āAGetSigninReportsWithCert.ps1 �t�@�C�����J���A�ȉ��� 3 �s���m�F�������ʂɍ��킹�ĕύX���܂��B

`$tenantId = "yourtenant.onmicrosoft.com"`

`$clientID = "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"`

`$thumprint = "0123456789ABCDEF0123456789ABCDEF01234567"`

�Ō�ɁAGetSigninReportsWithCert.ps1 �����s���܂��B����ɂ��T�C���C�� �A�N�e�B�r�e�B ���|�[�g�� csv �t�@�C���Ƃ��Ď擾�ł��܂��B