- 👋 Hi, I’m @dhacker002
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
dhacker002/dhacker002 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
    <PackageReference Include="System.ComponentModel.Primitives" Version="4.3.0 " />
    <PackageReference Include="System.ComponentModel.TypeConverter" Version="4.3.0" />
    <PackageReference Include="System.Data.Common" Version="4.3.0" />
    <PackageReference Include="System.Diagnostics.Process" Version="4.3.0" />
    <PackageReference Include="System.Diagnostics.StackTrace" Version="4.3.0" />
    <PackageReference Include="System.Diagnostics.TraceSource" Version="4.3.0" />
    <PackageReference Include="System.IO.FileSystem.Watcher" Version="4.3.0" />
    <PackageReference Include="System.Net.Http" Version="4.3.4" />
    <PackageReference Include="System.Net.NameResolution" Version="4.3.0" />
    <PackageReference Include="System.Net.Requests" Version="4.3.0" />
    <PackageReference Include="System.Reflection.TypeExtensions" Version="4.3.0" />
    <PackageReference Include="System.Runtime.Loader" Version="4.3.0" />
    <PackageReference Include="System.Text.RegularExpressions" Version="4.3.1" />
    <PackageReference Include="System.Threading.Thread" Version="4.3.0" />
    <PackageReference Include="System.Xml.XmlDocument" Version="4.3.0" />
  </ItemGroup>



 
  
    <ItemGroup Condition=" '$(TargetFramework)' ==
  'netstandard1.3' ">


  
 
 
  
      <PackageReference Include="System.ComponentModel.Primitives" Version="4.3.0"
  />


  
 
 
  
      <PackageReference Include="System.ComponentModel.TypeConverter" Version="4.3.0"
  />    <PackageReference Include="System.Data.Common" Version="4.3.0" />
    <PackageReference Include="System.Diagnostics.StackTrace" Version="4.3.0" />
    <PackageReference Include="System.Net.Http" Version="4.3.4" />
    <PackageReference Include="System.Net.NameResolution" Version="4.3.0" />
    <PackageReference Include="System.Net.Requests" Version="4.3.0" />
    <PackageReference Include="System.Reflection.TypeExtensions" Version="4.3.0" />
    <PackageReference Include="System.Text.RegularExpressions" Version="4.3.1" />
    <PackageReference Include="System.Xml.XmlDocument" Version="4.3.0" />
  </ItemGroup>


  <ItemGroup Condition=" '$(monobuild)' != '' ">
    <Reference Include="Mono.Posix" />
  </ItemGroup>
  
  <ItemGroup>
    <None Update="Common\InternalLogger-generated.tt">
      <Generator>TextTemplatingFileGenerator</Generator>
      <LastGenOutput>InternalLogger-generated.cs</LastGenOutput>
    </None>
    <None Update="Logger-generated.tt">
      <Generator>TextTemplatingFileGenerator</Generator>
      <LastGenOutput>Logger-generated.cs</LastGenOutput>
    </None>
  </ItemGroup>


  <ItemGroup>
    <Service Include="{508349b6-6b84-4df5-91f0-309beebad82d}" />
  </ItemGroup>


  <ItemGroup>
    <Compile Update="Common\InternalLogger-generated.cs">
      <DesignTime>True</DesignTime>
      <AutoGen>True</AutoGen>
      <DependentUpon>InternalLogger-generated.tt</DependentUpon>
    </Compile>
    <Compile Update="Logger-generated.cs">
      <DesignTime>True</DesignTime>
      <AutoGen>True</AutoGen>
      <DependentUpon>Logger-generated.tt</DependentUpon>
    </Compile>
  </ItemGroup>


  <PropertyGroup>
    <AssemblyTitle>$(Title)</AssemblyTitle>
    <!-- SonarQube WARNING: The following projects do not have a valid ProjectGuid and were not built using a valid solution (.sln) thus will be skipped from analysis… -->
    <ProjectGuid>{A0BFF0DB-ED9A-4639-AE86-8E709A1EFC66}</ProjectGuid>
    <ApplicationIcon>Resources\NLog.ico</ApplicationIcon>
  </PropertyGroup>


  <Target Name="PreBuild" BeforeTargets="PreBuildEvent">
    <Exec Command="echo building $(TargetFramework) ..." />
  </Target>


  <ItemGroup>
    <None Include="N.png" Pack="true" PackagePath="" Visible="false" />
  </ItemGroup>
  <Target Name="DownloadMissingContent" BeforeTargets="GenerateNuspec">
    <DownloadFile SourceUrl="https://nlog-project.org/N.png" DestinationFolder="$(MSBuildThisFileDirectory)" />
  </Target>


</Project>



  
 
