# StringProtector_NET5
This package contains strings protect method wite AES core


namespace IEB6440.StringProtector.NET5

For encrypt string use ProtectString classes static Encrypt(string plantstring, string key, bool keyAsBase64 = true) method and send the plant text to protect it, key as basic text ot base64 format (if you use basic text format send false to keyAsBase64 parameter)


For decrypt string use ProtectString classes static Decrypt(string cryptedstring, string key, bool keyAsBase64 = true) method and send the protected text to decrypt it use a sample key, key as basic text ot base64 format (if you use basic text format send false to keyAsBase64 parameter)

Exmple:

string KEY = "abecyha4u3ywqcb4c764btqn4c";

string planttext = "Some Sample Text";
string protectedstring = string.Empty;

protectedstring = ProtectString.Encrypt(planttext, KEY, false);

var reEncryptedstring = ProtectString.Decrypt(protectedstring, KEY, false);
