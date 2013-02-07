## -- Rsync Deploy config -- ##
deploy_default = "s3"
s3_bucket      = "www.amdavidson.me"

## -- Misc Configs -- ##

public_dir      = "public"    # compiled site directory
deploy_dir      = "_deploy"   # deploy directory (for Github pages deployment)

##############
# Deploying  #
##############

desc "Deploy website via s3cmd"
task :deploy do
  puts "## Deploying website via s3cmd"
  system("s3cmd sync --acl-public --reduced-redundancy #{public_dir}/* s3://#{s3_bucket}/")
end
