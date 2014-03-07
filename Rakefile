require 'fileutils'

def common_exists file
  @common_path ||= File.join Dir.pwd, 'modules', 'source', 'common'
  path = File.join @common_path, file + '.md'

  File.exists?(path) ? path : false
end

def process_include markdown
  # !![filename]
  markdown.gsub(/\!!\[(.*?)\]/m) do
    path = common_exists $1
    path ? File.read(path) : ''
  end
end

# process all include tags contained within the markdown
def generate_markdown
  base_path = File.join Dir.pwd, 'modules'
  src_path = File.join base_path, 'source', 'appium', '**', '*.md'
  dst_path = File.join base_path, 'gen'

  Dir.glob(src_path) do |md|
    new_path = File.join(dst_path, md.gsub(File.join(base_path, 'source'), ''))
    FileUtils.mkdir_p File.dirname new_path # ensure full path exists
    data = process_include File.read md
    File.open(new_path, 'w') { |f| f.write data }
  end
end

desc 'Generate markdown from modules/source into modules/gen'
task :default do
  generate_markdown
end